---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGateway.md
ms.openlocfilehash: 4b94c3e0d178748169b5faaa3b7eb43b76f8bc4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531066"
---
# <span data-ttu-id="60fca-101">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="60fca-101">New-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="60fca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60fca-102">SYNOPSIS</span></span>
<span data-ttu-id="60fca-103">Azure Data Factory에 대 한 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60fca-103">Creates a gateway for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60fca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60fca-104">SYNTAX</span></span>

### <span data-ttu-id="60fca-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="60fca-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60fca-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="60fca-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60fca-107">설명은</span><span class="sxs-lookup"><span data-stu-id="60fca-107">DESCRIPTION</span></span>
<span data-ttu-id="60fca-108">**새 AzureRmDataFactoryGateway** Cmdlet은 Azure Data Factory에서 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60fca-108">The **New-AzureRmDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="60fca-109">예제의</span><span class="sxs-lookup"><span data-stu-id="60fca-109">EXAMPLES</span></span>

### <span data-ttu-id="60fca-110">예제 1: 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="60fca-110">Example 1: Create a gateway</span></span>
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

<span data-ttu-id="60fca-111">이 명령은 ADF 라는 리소스 그룹의 WikiADF 이라는 data factory에 ContosoGateway 이라는 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60fca-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="60fca-112">변수</span><span class="sxs-lookup"><span data-stu-id="60fca-112">PARAMETERS</span></span>

### <span data-ttu-id="60fca-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="60fca-113">-DataFactory</span></span>
<span data-ttu-id="60fca-114">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fca-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="60fca-115">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 대 한 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60fca-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60fca-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="60fca-116">-DataFactoryName</span></span>
<span data-ttu-id="60fca-117">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fca-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="60fca-118">이 cmdlet은이 매개 변수에서 지정 하는 data factory에 대 한 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60fca-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60fca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60fca-119">-DefaultProfile</span></span>
<span data-ttu-id="60fca-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="60fca-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60fca-121">-설명</span><span class="sxs-lookup"><span data-stu-id="60fca-121">-Description</span></span>
<span data-ttu-id="60fca-122">게이트웨이에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fca-122">Specifies a description for the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60fca-123">-이름</span><span class="sxs-lookup"><span data-stu-id="60fca-123">-Name</span></span>
<span data-ttu-id="60fca-124">만들 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fca-124">Specifies the name of the gateway to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60fca-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60fca-125">-ResourceGroupName</span></span>
<span data-ttu-id="60fca-126">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fca-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="60fca-127">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60fca-127">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60fca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60fca-128">CommonParameters</span></span>
<span data-ttu-id="60fca-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60fca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60fca-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60fca-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60fca-131">입력</span><span class="sxs-lookup"><span data-stu-id="60fca-131">INPUTS</span></span>

### <span data-ttu-id="60fca-132">않아야</span><span class="sxs-lookup"><span data-stu-id="60fca-132">None</span></span>
<span data-ttu-id="60fca-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60fca-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="60fca-134">출력</span><span class="sxs-lookup"><span data-stu-id="60fca-134">OUTPUTS</span></span>

### <span data-ttu-id="60fca-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="60fca-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="60fca-136">상속자</span><span class="sxs-lookup"><span data-stu-id="60fca-136">NOTES</span></span>
* <span data-ttu-id="60fca-137">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="60fca-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="60fca-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60fca-138">RELATED LINKS</span></span>

[<span data-ttu-id="60fca-139">제거-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="60fca-139">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="60fca-140">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="60fca-140">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


