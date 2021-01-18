---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
ms.openlocfilehash: 6d7b82a3046b56b473140b6830a0b04333cba9b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493568"
---
# <span data-ttu-id="ebcb0-101">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="ebcb0-101">Get-AzDataFactoryGateway</span></span>

## <span data-ttu-id="ebcb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebcb0-102">SYNOPSIS</span></span>
<span data-ttu-id="ebcb0-103">Azure Data Factory의 논리 게이트웨이에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcb0-103">Gets information about logical gateways in Azure Data Factory.</span></span>

## <span data-ttu-id="ebcb0-104">구문</span><span class="sxs-lookup"><span data-stu-id="ebcb0-104">SYNTAX</span></span>

### <span data-ttu-id="ebcb0-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="ebcb0-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebcb0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ebcb0-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebcb0-107">설명</span><span class="sxs-lookup"><span data-stu-id="ebcb0-107">DESCRIPTION</span></span>
<span data-ttu-id="ebcb0-108">**Get-AzDataFactoryGateway** cmdlet은 Azure Data Factory의 논리 게이트웨이에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcb0-108">The **Get-AzDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="ebcb0-109">게이트웨이의 이름을 지정하는 경우 이 cmdlet은 해당 게이트웨이에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcb0-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="ebcb0-110">이름을 지정하지 않으면 이 cmdlet은 데이터 팩터리의 모든 게이트웨이에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcb0-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>
<span data-ttu-id="ebcb0-111">데이터 팩터리에 연결된 서비스로 Microsoft SQL Server 프레미스 서비스를 추가하려는 경우 게이트웨이를 On-프레미스 컴퓨터에 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcb0-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="ebcb0-112">예제</span><span class="sxs-lookup"><span data-stu-id="ebcb0-112">EXAMPLES</span></span>

### <span data-ttu-id="ebcb0-113">예제 1: 데이터 팩터리의 모든 논리 게이트웨이를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcb0-113">Example 1: Get all logical gateways in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
Name            : gateway1
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      : 
Name            : gateway2
Description     : 
Version         : 1.3.5338.1
Status          : Offline
VersionStatus   : UpToDate
CreateTime      : 8/29/2014 1:46:44 AM
RegisterTime    : 8/29/2014 1:48:36 AM
LastConnectTime : 8/29/2014 1:56:56 AM
ExpiryTime      :
```

<span data-ttu-id="ebcb0-114">이 명령은 ADF라는 리소스 그룹의 WikiADF라는 데이터 팩터리에 대한 모든 논리 게이트웨이에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcb0-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="ebcb0-115">예제 2: 데이터 팩터리에서 특정 논리 게이트웨이를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcb0-115">Example 2: Get a specific logical gateway in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "Gateway01" -DataFactoryName "WikiADF"
Name            : Gateway01
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      :
```

<span data-ttu-id="ebcb0-116">이 명령은 ADF라는 리소스 그룹의 WikiADF라는 데이터 팩터리에서 Gateway01이라는 논리 게이트웨이에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcb0-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="ebcb0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebcb0-117">PARAMETERS</span></span>

### <span data-ttu-id="ebcb0-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ebcb0-118">-DataFactory</span></span>
<span data-ttu-id="ebcb0-119">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="ebcb0-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ebcb0-120">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리의 논리 게이트웨이에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcb0-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ebcb0-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ebcb0-121">-DataFactoryName</span></span>
<span data-ttu-id="ebcb0-122">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcb0-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ebcb0-123">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리의 논리 게이트웨이에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcb0-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ebcb0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebcb0-124">-DefaultProfile</span></span>
<span data-ttu-id="ebcb0-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ebcb0-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebcb0-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ebcb0-126">-Name</span></span>
<span data-ttu-id="ebcb0-127">정보를 얻을 논리 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcb0-127">Specifies the name of the logical gateway about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebcb0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebcb0-128">-ResourceGroupName</span></span>
<span data-ttu-id="ebcb0-129">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcb0-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ebcb0-130">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 논리 게이트웨이에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcb0-130">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ebcb0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebcb0-131">CommonParameters</span></span>
<span data-ttu-id="ebcb0-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcb0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebcb0-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ebcb0-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebcb0-134">입력</span><span class="sxs-lookup"><span data-stu-id="ebcb0-134">INPUTS</span></span>

### <span data-ttu-id="ebcb0-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ebcb0-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="ebcb0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ebcb0-136">System.String</span></span>

## <span data-ttu-id="ebcb0-137">출력</span><span class="sxs-lookup"><span data-stu-id="ebcb0-137">OUTPUTS</span></span>

### <span data-ttu-id="ebcb0-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="ebcb0-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="ebcb0-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ebcb0-139">NOTES</span></span>
* <span data-ttu-id="ebcb0-140">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="ebcb0-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ebcb0-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ebcb0-141">RELATED LINKS</span></span>

[<span data-ttu-id="ebcb0-142">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="ebcb0-142">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="ebcb0-143">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="ebcb0-143">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="ebcb0-144">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="ebcb0-144">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


