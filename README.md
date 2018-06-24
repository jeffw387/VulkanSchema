# VulkanSchema
Aims to allow vulkan to be configured with json.

The schema folder contains the schema for the config jsons. 
They are named with the pattern "module.schema.json" where module 
is the name of the json object.

Module names are intended to match the vulkan types except without the "Vk" prefix,
and they use camelCase. They also replace "CreateInfo" and "StateCreateInfo" with
"Config", though I'm not sure this is ideal. I'm open to changing it to match Vulkan
more directly.

Most modules have a "uri" field (possibly not a good name?) that I planned to fill
with a file name in order to allow modular construction of vulkan structures.
In many cases a module can either be inline or can be referred to by "uri".