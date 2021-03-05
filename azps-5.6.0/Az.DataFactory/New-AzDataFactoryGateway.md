---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
ms.openlocfilehash: 04026cf8cc01e1733c44821824ca4b0682b2b66d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974971"
---
# <span data-ttu-id="22c19-101">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="22c19-101">New-AzDataFactoryGateway</span></span>

## <span data-ttu-id="22c19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22c19-102">SYNOPSIS</span></span>
<span data-ttu-id="22c19-103">Azure Data Factory에 대한 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22c19-103">Creates a gateway for an Azure Data Factory.</span></span>

## <span data-ttu-id="22c19-104">구문</span><span class="sxs-lookup"><span data-stu-id="22c19-104">SYNTAX</span></span>

### <span data-ttu-id="22c19-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="22c19-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22c19-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="22c19-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22c19-107">설명</span><span class="sxs-lookup"><span data-stu-id="22c19-107">DESCRIPTION</span></span>
<span data-ttu-id="22c19-108">**New-AzDataFactoryGateway** cmdlet은 Azure Data Factory에서 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22c19-108">The **New-AzDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="22c19-109">예제</span><span class="sxs-lookup"><span data-stu-id="22c19-109">EXAMPLES</span></span>

### <span data-ttu-id="22c19-110">예제 1: 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="22c19-110">Example 1: Create a gateway</span></span>
```
PS C:\>New-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
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

<span data-ttu-id="22c19-111">이 명령은 ADF라는 리소스 그룹의 WikiADF라는 데이터 팩터리에 ContosoGateway라는 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22c19-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="22c19-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="22c19-112">PARAMETERS</span></span>

### <span data-ttu-id="22c19-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="22c19-113">-DataFactory</span></span>
<span data-ttu-id="22c19-114">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="22c19-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="22c19-115">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 대한 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22c19-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="22c19-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="22c19-116">-DataFactoryName</span></span>
<span data-ttu-id="22c19-117">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22c19-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="22c19-118">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 대한 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22c19-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="22c19-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22c19-119">-DefaultProfile</span></span>
<span data-ttu-id="22c19-120">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="22c19-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c19-121">-Description</span><span class="sxs-lookup"><span data-stu-id="22c19-121">-Description</span></span>
<span data-ttu-id="22c19-122">게이트웨이에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22c19-122">Specifies a description for the gateway.</span></span>

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

### <span data-ttu-id="22c19-123">-Name</span><span class="sxs-lookup"><span data-stu-id="22c19-123">-Name</span></span>
<span data-ttu-id="22c19-124">만들 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22c19-124">Specifies the name of the gateway to create.</span></span>

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

### <span data-ttu-id="22c19-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22c19-125">-ResourceGroupName</span></span>
<span data-ttu-id="22c19-126">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22c19-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="22c19-127">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22c19-127">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="22c19-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c19-128">CommonParameters</span></span>
<span data-ttu-id="22c19-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="22c19-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c19-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="22c19-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c19-131">입력</span><span class="sxs-lookup"><span data-stu-id="22c19-131">INPUTS</span></span>

### <span data-ttu-id="22c19-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="22c19-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="22c19-133">System.String</span><span class="sxs-lookup"><span data-stu-id="22c19-133">System.String</span></span>

## <span data-ttu-id="22c19-134">출력</span><span class="sxs-lookup"><span data-stu-id="22c19-134">OUTPUTS</span></span>

### <span data-ttu-id="22c19-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="22c19-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="22c19-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="22c19-136">NOTES</span></span>
* <span data-ttu-id="22c19-137">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="22c19-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="22c19-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22c19-138">RELATED LINKS</span></span>

[<span data-ttu-id="22c19-139">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="22c19-139">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="22c19-140">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="22c19-140">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


