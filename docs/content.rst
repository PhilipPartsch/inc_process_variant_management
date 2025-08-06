#######
Content
#######

.. req:: Example requirement one
   :id: R_EXAMPLE_REQUIREMENT_ONE
   :status: draft

   Set safety_state and security_state to default values.

.. req:: Example requirement two
   :id: R_EXAMPLE_REQUIREMENT_TWO
   :status: QNX:accepted,Linux:draft,draft
   :safety_state: QNX:ASIL_D,Linux:ASIL_B,QM
   :security_state: Yes

   Set safety_state is set by variant management to :ndf:`copy("safety_state")`.

.. if:: OS == "Linux"

   .. req:: Variant Linux
      :id: R_LINUX
      :status: accepted
      :safety_state: ASIL_B
      :security_state: Yes

      Requirement to support Linux as OS.

.. elif:: OS == "QNX"

   .. req:: Variant QNX
      :id: R_QNX
      :status: accepted
      :safety_state: ASIL_B
      :security_state: Yes

      Requirement to support QNX as OS.

.. else::

   .. req:: Variant OS undefined
      :id: R_UNDEFINED_OS
      :status: accepted
      :safety_state: QM
      :security_state: No

      Requirement to support undfined OS as OS.

.. spec:: Example specification one
   :id: R_EXAMPLE_SPECIFICATION_ONE
   :status: draft

   Set safety_state and security_state to default values.

.. spec:: Example specification two
   :id: R_EXAMPLE_SPECIFICATION_TWO
   :status: draft
   :safety_state: ASIL_B
   :security_state: Yes
   :satisfies: QNX:R_QNX,Linux:R_LINUX

   Set safety_state manual to ASIL_B and security_state manual to Yes.
