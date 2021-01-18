---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
ms.openlocfilehash: b9eebe26e64e9a7ce2497cdf9984ca6dabb062e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493515"
---
# <span data-ttu-id="7a163-101">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="7a163-101">Set-AzDataFactoryGateway</span></span>

## <span data-ttu-id="7a163-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a163-102">SYNOPSIS</span></span>
<span data-ttu-id="7a163-103">Azure Data Factory에서 게이트웨이에 대한 설명을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a163-103">Sets the description for a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="7a163-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a163-104">SYNTAX</span></span>

### <span data-ttu-id="7a163-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="7a163-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a163-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7a163-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a163-107">설명</span><span class="sxs-lookup"><span data-stu-id="7a163-107">DESCRIPTION</span></span>
<span data-ttu-id="7a163-108">**Set-AzDataFactoryGateway** cmdlet은 Azure Data Factory에서 지정된 게이트웨이에 대한 설명을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a163-108">The **Set-AzDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="7a163-109">예제</span><span class="sxs-lookup"><span data-stu-id="7a163-109">EXAMPLES</span></span>

### <span data-ttu-id="7a163-110">예제 1: 게이트웨이에 대한 설명 설정</span><span class="sxs-lookup"><span data-stu-id="7a163-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name            : ContosoGateway
Description     : my gateway
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:31:09 AM
RegisterTime    : 8/22/2014 1:31:37 AM
LastConnectTime : 8/22/2014 1:41:41 AM
ExpiryTime      :
```

<span data-ttu-id="7a163-111">이 명령은 WikiADF라는 데이터 팩터리에서 ContosoGateway라는 게이트웨이에 대한 설명을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a163-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="7a163-112">Description 매개 변수는 새 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a163-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="7a163-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a163-113">PARAMETERS</span></span>

### <span data-ttu-id="7a163-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7a163-114">-DataFactory</span></span>
<span data-ttu-id="7a163-115">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="7a163-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="7a163-116">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리의 게이트웨이에 대한 설명을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a163-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7a163-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7a163-117">-DataFactoryName</span></span>
<span data-ttu-id="7a163-118">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a163-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7a163-119">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리의 게이트웨이에 대한 설명을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a163-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7a163-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a163-120">-DefaultProfile</span></span>
<span data-ttu-id="7a163-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7a163-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a163-122">-Description</span><span class="sxs-lookup"><span data-stu-id="7a163-122">-Description</span></span>
<span data-ttu-id="7a163-123">게이트웨이에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a163-123">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a163-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7a163-124">-Name</span></span>
<span data-ttu-id="7a163-125">설명을 설정할 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a163-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="7a163-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a163-126">-ResourceGroupName</span></span>
<span data-ttu-id="7a163-127">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a163-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7a163-128">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속한 게이트웨이에 대한 설명을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a163-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7a163-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a163-129">CommonParameters</span></span>
<span data-ttu-id="7a163-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a163-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a163-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7a163-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a163-132">입력</span><span class="sxs-lookup"><span data-stu-id="7a163-132">INPUTS</span></span>

### <span data-ttu-id="7a163-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7a163-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="7a163-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7a163-134">System.String</span></span>

## <span data-ttu-id="7a163-135">출력</span><span class="sxs-lookup"><span data-stu-id="7a163-135">OUTPUTS</span></span>

### <span data-ttu-id="7a163-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="7a163-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="7a163-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a163-137">NOTES</span></span>
* <span data-ttu-id="7a163-138">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="7a163-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7a163-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a163-139">RELATED LINKS</span></span>

[<span data-ttu-id="7a163-140">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="7a163-140">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="7a163-141">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="7a163-141">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="7a163-142">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="7a163-142">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)


