---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFB0000C-2EFF-4216-923B-55B0B07BFE60
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51ab7d137fbbac1925ae689a1dcb16c89b9b8000
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045606"
---
# <span data-ttu-id="f55ac-101">Get-AzureServiceAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="f55ac-101">Get-AzureServiceAvailableExtension</span></span>

## <span data-ttu-id="f55ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f55ac-102">SYNOPSIS</span></span>
<span data-ttu-id="f55ac-103">호스팅된 서비스에 사용할 수 있는 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f55ac-103">Gets information about the available extensions for hosted services.</span></span>

## <span data-ttu-id="f55ac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f55ac-104">SYNTAX</span></span>

### <span data-ttu-id="f55ac-105">ListLatestExtensions (기본값)</span><span class="sxs-lookup"><span data-stu-id="f55ac-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureServiceAvailableExtension [[-ExtensionName] <String>] [[-ProviderNamespace] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f55ac-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="f55ac-106">ListAllVersions</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f55ac-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="f55ac-107">ListSingleVersion</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="f55ac-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f55ac-108">DESCRIPTION</span></span>
<span data-ttu-id="f55ac-109">**Get-Azureserviceavailable extension** cmdlet은 호스팅된 서비스에 대해 사용 가능한 최신 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f55ac-109">The **Get-AzureServiceAvailableExtension** cmdlet gets information for the latest available extensions for hosted services.</span></span>

## <span data-ttu-id="f55ac-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f55ac-110">EXAMPLES</span></span>

### <span data-ttu-id="f55ac-111">예제 1: 사용할 수 있는 확장 가져오기</span><span class="sxs-lookup"><span data-stu-id="f55ac-111">Example 1: Get available extensions</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="f55ac-112">이 명령은 사용 가능한 모든 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f55ac-112">This command gets all available extensions.</span></span>

### <span data-ttu-id="f55ac-113">예제 2: 지정 된 네임 스페이스에 확장 가져오기</span><span class="sxs-lookup"><span data-stu-id="f55ac-113">Example 2: Get extensions in a specified namespace</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -AllVersions

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="f55ac-114">이 명령은 지정 된 이름 공간에서 지정한 이름의 확장명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f55ac-114">This command gets the extensions with a specified name in a specified namespace.</span></span>

### <span data-ttu-id="f55ac-115">예제 3: 특정 버전의 확장 가져오기</span><span class="sxs-lookup"><span data-stu-id="f55ac-115">Example 3: Get a specific version of an extension</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -Version 1.0.0.1

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="f55ac-116">이 명령은 특정 버전의 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f55ac-116">This command gets information about a specific version of an extension.</span></span>

## <span data-ttu-id="f55ac-117">변수</span><span class="sxs-lookup"><span data-stu-id="f55ac-117">PARAMETERS</span></span>

### <span data-ttu-id="f55ac-118">-AllVersions</span><span class="sxs-lookup"><span data-stu-id="f55ac-118">-AllVersions</span></span>
<span data-ttu-id="f55ac-119">이 cmdlet이 확장의 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f55ac-119">Indicates that this cmdlet gets all versions of an extension.</span></span>

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

### <span data-ttu-id="f55ac-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="f55ac-120">-ExtensionName</span></span>
<span data-ttu-id="f55ac-121">확장명 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f55ac-121">Specifies the extension name.</span></span>

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

### <span data-ttu-id="f55ac-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f55ac-122">-InformationAction</span></span>
<span data-ttu-id="f55ac-123">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f55ac-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f55ac-124">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f55ac-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f55ac-125">하기로</span><span class="sxs-lookup"><span data-stu-id="f55ac-125">Continue</span></span>
- <span data-ttu-id="f55ac-126">숨기기</span><span class="sxs-lookup"><span data-stu-id="f55ac-126">Ignore</span></span>
- <span data-ttu-id="f55ac-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="f55ac-127">Inquire</span></span>
- <span data-ttu-id="f55ac-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f55ac-128">SilentlyContinue</span></span>
- <span data-ttu-id="f55ac-129">중지가</span><span class="sxs-lookup"><span data-stu-id="f55ac-129">Stop</span></span>
- <span data-ttu-id="f55ac-130">대기</span><span class="sxs-lookup"><span data-stu-id="f55ac-130">Suspend</span></span>

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

### <span data-ttu-id="f55ac-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f55ac-131">-InformationVariable</span></span>
<span data-ttu-id="f55ac-132">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f55ac-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f55ac-133">-프로필</span><span class="sxs-lookup"><span data-stu-id="f55ac-133">-Profile</span></span>
<span data-ttu-id="f55ac-134">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f55ac-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f55ac-135">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f55ac-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f55ac-136">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="f55ac-136">-ProviderNamespace</span></span>
<span data-ttu-id="f55ac-137">확장 공급자 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f55ac-137">Specifies the extension provider namespace.</span></span>

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

### <span data-ttu-id="f55ac-138">-버전</span><span class="sxs-lookup"><span data-stu-id="f55ac-138">-Version</span></span>
<span data-ttu-id="f55ac-139">확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f55ac-139">Specifies the extension version.</span></span>

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

### <span data-ttu-id="f55ac-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55ac-140">CommonParameters</span></span>
<span data-ttu-id="f55ac-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f55ac-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55ac-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f55ac-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55ac-143">입력</span><span class="sxs-lookup"><span data-stu-id="f55ac-143">INPUTS</span></span>

## <span data-ttu-id="f55ac-144">출력</span><span class="sxs-lookup"><span data-stu-id="f55ac-144">OUTPUTS</span></span>

## <span data-ttu-id="f55ac-145">상속자</span><span class="sxs-lookup"><span data-stu-id="f55ac-145">NOTES</span></span>

## <span data-ttu-id="f55ac-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f55ac-146">RELATED LINKS</span></span>

[<span data-ttu-id="f55ac-147">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="f55ac-147">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)


