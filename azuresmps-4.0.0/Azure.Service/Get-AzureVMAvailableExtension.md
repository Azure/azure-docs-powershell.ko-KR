---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAC3DABB-8230-4E86-9936-0F1848980EA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: d062b4300af2efbd45bfccd7ed467871b23d8256
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046544"
---
# <span data-ttu-id="505d5-101">Get-AzureVMAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="505d5-101">Get-AzureVMAvailableExtension</span></span>

## <span data-ttu-id="505d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="505d5-102">SYNOPSIS</span></span>
<span data-ttu-id="505d5-103">가상 컴퓨터에 대해 사용 가능한 최신 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="505d5-103">Gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="505d5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="505d5-104">SYNTAX</span></span>

### <span data-ttu-id="505d5-105">ListLatestExtensions (기본값)</span><span class="sxs-lookup"><span data-stu-id="505d5-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureVMAvailableExtension [[-ExtensionName] <String>] [[-Publisher] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="505d5-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="505d5-106">ListAllVersions</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="505d5-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="505d5-107">ListSingleVersion</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="505d5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="505d5-108">DESCRIPTION</span></span>
<span data-ttu-id="505d5-109">**AzureVMAvailableExtension** cmdlet은 가상 컴퓨터에 대해 사용 가능한 최신 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="505d5-109">The **Get-AzureVMAvailableExtension** cmdlet gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="505d5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="505d5-110">EXAMPLES</span></span>

### <span data-ttu-id="505d5-111">예제 1: 사용 가능한 최신 확장에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="505d5-111">Example 1: Get information for the latest available extensions</span></span>
```
PS C:\> Get-AzureVMAvailableExtension
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="505d5-112">이 명령은 모든 가상 컴퓨터에 대해 사용 가능한 최신 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="505d5-112">This command gets information for the latest available extensions for all virtual machines.</span></span>

### <span data-ttu-id="505d5-113">예제 2: 지정 된 확장명 이름으로 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="505d5-113">Example 2: Get information from a specified extension name</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName "VMAccessAgent" -AllVersions
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.2
          PublicConfigurationSchema  : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          PrivateConfigurationSchema : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded

          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="505d5-114">이 명령은 VMAccessAgent 이라는 모든 버전의 확장명 및 Microsoft 컴퓨터인 게시자의 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="505d5-114">This command gets information from all versions of the extension named VMAccessAgent and the publisher named Microsoft.Computer.</span></span>

### <span data-ttu-id="505d5-115">예제 3: 버전 번호로 특정 가상 컴퓨터 확장에서 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="505d5-115">Example 3: Get information from a specific virtual machine extension by version number</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName VMAccessAgent -Version 1.0.3
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="505d5-116">이 명령은 VMAccessAgent 이라는 확장명에 대 한 정보를 가져오고 확장 버전 1.0.3에 대해 Microsoft 라는 게시자를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="505d5-116">This command gets information for the extension named VMAccessAgent and the publisher named Microsoft.Compute for the extension version 1.0.3.</span></span>

## <span data-ttu-id="505d5-117">변수</span><span class="sxs-lookup"><span data-stu-id="505d5-117">PARAMETERS</span></span>

### <span data-ttu-id="505d5-118">-AllVersions</span><span class="sxs-lookup"><span data-stu-id="505d5-118">-AllVersions</span></span>
<span data-ttu-id="505d5-119">이 cmdlet에 모든 확장 버전의 목록이 표시 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="505d5-119">Indicates that this cmdlet lists all versions of an extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAllVersions
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="505d5-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="505d5-120">-ExtensionName</span></span>
<span data-ttu-id="505d5-121">사용할 수 있는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="505d5-121">Specifies the name of the available extension.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="505d5-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="505d5-122">-InformationAction</span></span>
<span data-ttu-id="505d5-123">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="505d5-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="505d5-124">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="505d5-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="505d5-125">하기로</span><span class="sxs-lookup"><span data-stu-id="505d5-125">Continue</span></span>
- <span data-ttu-id="505d5-126">숨기기</span><span class="sxs-lookup"><span data-stu-id="505d5-126">Ignore</span></span>
- <span data-ttu-id="505d5-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="505d5-127">Inquire</span></span>
- <span data-ttu-id="505d5-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="505d5-128">SilentlyContinue</span></span>
- <span data-ttu-id="505d5-129">중지가</span><span class="sxs-lookup"><span data-stu-id="505d5-129">Stop</span></span>
- <span data-ttu-id="505d5-130">대기</span><span class="sxs-lookup"><span data-stu-id="505d5-130">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="505d5-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="505d5-131">-InformationVariable</span></span>
<span data-ttu-id="505d5-132">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="505d5-132">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="505d5-133">-프로필</span><span class="sxs-lookup"><span data-stu-id="505d5-133">-Profile</span></span>
<span data-ttu-id="505d5-134">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="505d5-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="505d5-135">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="505d5-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="505d5-136">-Publisher</span><span class="sxs-lookup"><span data-stu-id="505d5-136">-Publisher</span></span>
<span data-ttu-id="505d5-137">확장의 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="505d5-137">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="505d5-138">-버전</span><span class="sxs-lookup"><span data-stu-id="505d5-138">-Version</span></span>
<span data-ttu-id="505d5-139">확장의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="505d5-139">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListSingleVersion
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="505d5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="505d5-140">CommonParameters</span></span>
<span data-ttu-id="505d5-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="505d5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="505d5-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="505d5-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="505d5-143">입력</span><span class="sxs-lookup"><span data-stu-id="505d5-143">INPUTS</span></span>

## <span data-ttu-id="505d5-144">출력</span><span class="sxs-lookup"><span data-stu-id="505d5-144">OUTPUTS</span></span>

## <span data-ttu-id="505d5-145">상속자</span><span class="sxs-lookup"><span data-stu-id="505d5-145">NOTES</span></span>

## <span data-ttu-id="505d5-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="505d5-146">RELATED LINKS</span></span>

