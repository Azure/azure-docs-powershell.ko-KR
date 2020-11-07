---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
ms.openlocfilehash: da5ae19a03b34a04fc9928d684910e759303cedd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697084"
---
# <span data-ttu-id="b9c5d-101">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b9c5d-101">Get-AzDataFactoryGateway</span></span>

## <span data-ttu-id="b9c5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c5d-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c5d-103">Azure Data Factory의 논리 게이트웨이에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9c5d-103">Gets information about logical gateways in Azure Data Factory.</span></span>

## <span data-ttu-id="b9c5d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b9c5d-104">SYNTAX</span></span>

### <span data-ttu-id="b9c5d-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b9c5d-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9c5d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b9c5d-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9c5d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b9c5d-107">DESCRIPTION</span></span>
<span data-ttu-id="b9c5d-108">**AzDataFactoryGateway** Cmdlet은 Azure Data Factory의 논리 게이트웨이에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9c5d-108">The **Get-AzDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="b9c5d-109">게이트웨이의 이름을 지정 하는 경우이 cmdlet은 해당 게이트웨이에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9c5d-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="b9c5d-110">이름을 지정 하지 않으면이 cmdlet은 data factory의 모든 게이트웨이에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9c5d-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>
<span data-ttu-id="b9c5d-111">온-프레미스 Microsoft SQL Server를 data factory에 연결 된 서비스로 추가 하려면 온-프레미스 컴퓨터에 게이트웨이를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c5d-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="b9c5d-112">예제의</span><span class="sxs-lookup"><span data-stu-id="b9c5d-112">EXAMPLES</span></span>

### <span data-ttu-id="b9c5d-113">예제 1: 데이터 팩터리에 모든 논리 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="b9c5d-113">Example 1: Get all logical gateways in a data factory</span></span>
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

<span data-ttu-id="b9c5d-114">이 명령은 ADF 라는 리소스 그룹에 있는 WikiADF 이라는 data factory의 모든 논리 게이트웨이에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9c5d-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="b9c5d-115">예제 2: 데이터 팩터리에 특정 논리 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="b9c5d-115">Example 2: Get a specific logical gateway in a data factory</span></span>
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

<span data-ttu-id="b9c5d-116">이 명령은 ADF 라는 리소스 그룹의 WikiADF 이라는 data factory의 Gateway01 이라는 논리 게이트웨이에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9c5d-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="b9c5d-117">변수</span><span class="sxs-lookup"><span data-stu-id="b9c5d-117">PARAMETERS</span></span>

### <span data-ttu-id="b9c5d-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b9c5d-118">-DataFactory</span></span>
<span data-ttu-id="b9c5d-119">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c5d-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b9c5d-120">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 논리 게이트웨이에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9c5d-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b9c5d-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b9c5d-121">-DataFactoryName</span></span>
<span data-ttu-id="b9c5d-122">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c5d-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b9c5d-123">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 논리 게이트웨이에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9c5d-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b9c5d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c5d-124">-DefaultProfile</span></span>
<span data-ttu-id="b9c5d-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b9c5d-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9c5d-126">-이름</span><span class="sxs-lookup"><span data-stu-id="b9c5d-126">-Name</span></span>
<span data-ttu-id="b9c5d-127">정보를 가져올 논리 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c5d-127">Specifies the name of the logical gateway about which to get information.</span></span>

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

### <span data-ttu-id="b9c5d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c5d-128">-ResourceGroupName</span></span>
<span data-ttu-id="b9c5d-129">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c5d-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b9c5d-130">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 논리 게이트웨이에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9c5d-130">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b9c5d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c5d-131">CommonParameters</span></span>
<span data-ttu-id="b9c5d-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c5d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c5d-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c5d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c5d-134">입력</span><span class="sxs-lookup"><span data-stu-id="b9c5d-134">INPUTS</span></span>

### <span data-ttu-id="b9c5d-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b9c5d-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="b9c5d-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b9c5d-136">System.String</span></span>

## <span data-ttu-id="b9c5d-137">출력</span><span class="sxs-lookup"><span data-stu-id="b9c5d-137">OUTPUTS</span></span>

### <span data-ttu-id="b9c5d-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b9c5d-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="b9c5d-139">상속자</span><span class="sxs-lookup"><span data-stu-id="b9c5d-139">NOTES</span></span>
* <span data-ttu-id="b9c5d-140">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="b9c5d-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b9c5d-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9c5d-141">RELATED LINKS</span></span>

[<span data-ttu-id="b9c5d-142">새로운 AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b9c5d-142">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="b9c5d-143">제거-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b9c5d-143">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="b9c5d-144">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="b9c5d-144">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


