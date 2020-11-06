---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGateway.md
ms.openlocfilehash: 908c2b4804cf242642ce68adf0e28477fae40aac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530792"
---
# <span data-ttu-id="fc0b8-101">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="fc0b8-101">New-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="fc0b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc0b8-102">SYNOPSIS</span></span>
<span data-ttu-id="fc0b8-103">Azure Data Factory에 대 한 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc0b8-103">Creates a gateway for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc0b8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc0b8-104">SYNTAX</span></span>

### <span data-ttu-id="fc0b8-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="fc0b8-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc0b8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fc0b8-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc0b8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fc0b8-107">DESCRIPTION</span></span>
<span data-ttu-id="fc0b8-108">**새 AzureRmDataFactoryGateway** Cmdlet은 Azure Data Factory에서 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc0b8-108">The **New-AzureRmDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="fc0b8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fc0b8-109">EXAMPLES</span></span>

### <span data-ttu-id="fc0b8-110">예제 1: 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="fc0b8-110">Example 1: Create a gateway</span></span>
```
PS C:\>New-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name              : ContosoGateway
Description       : my gateway
Version           : 
Status            : NeedRegistration
VersionStatus     : None
CreateTime        : 8/22/2014 1:40:34 AM
RegisterTime      : 
LastConnectTime   : 
ExpiryTime        : 
ProvisioningState : Succeeded
Key               : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="fc0b8-111">이 명령은 ADF 라는 리소스 그룹의 WikiADF 이라는 data factory에 ContosoGateway 이라는 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc0b8-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="fc0b8-112">변수</span><span class="sxs-lookup"><span data-stu-id="fc0b8-112">PARAMETERS</span></span>

### <span data-ttu-id="fc0b8-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fc0b8-113">-DataFactory</span></span>
<span data-ttu-id="fc0b8-114">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc0b8-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="fc0b8-115">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 대 한 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc0b8-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0b8-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fc0b8-116">-DataFactoryName</span></span>
<span data-ttu-id="fc0b8-117">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc0b8-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fc0b8-118">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 대 한 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc0b8-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0b8-119">-설명</span><span class="sxs-lookup"><span data-stu-id="fc0b8-119">-Description</span></span>
<span data-ttu-id="fc0b8-120">게이트웨이에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc0b8-120">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0b8-121">-이름</span><span class="sxs-lookup"><span data-stu-id="fc0b8-121">-Name</span></span>
<span data-ttu-id="fc0b8-122">만들 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc0b8-122">Specifies the name of the gateway to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0b8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc0b8-123">-ResourceGroupName</span></span>
<span data-ttu-id="fc0b8-124">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc0b8-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fc0b8-125">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc0b8-125">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0b8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc0b8-126">-DefaultProfile</span></span>
<span data-ttu-id="fc0b8-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc0b8-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc0b8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc0b8-128">CommonParameters</span></span>
<span data-ttu-id="fc0b8-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc0b8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc0b8-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc0b8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc0b8-131">입력</span><span class="sxs-lookup"><span data-stu-id="fc0b8-131">INPUTS</span></span>

## <span data-ttu-id="fc0b8-132">출력</span><span class="sxs-lookup"><span data-stu-id="fc0b8-132">OUTPUTS</span></span>

### <span data-ttu-id="fc0b8-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="fc0b8-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="fc0b8-134">상속자</span><span class="sxs-lookup"><span data-stu-id="fc0b8-134">NOTES</span></span>
* <span data-ttu-id="fc0b8-135">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="fc0b8-135">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fc0b8-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc0b8-136">RELATED LINKS</span></span>

[<span data-ttu-id="fc0b8-137">제거-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="fc0b8-137">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="fc0b8-138">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="fc0b8-138">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


