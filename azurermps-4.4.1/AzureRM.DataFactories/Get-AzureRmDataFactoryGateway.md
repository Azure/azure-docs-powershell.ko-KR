---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
ms.openlocfilehash: a90146480b0706d88f4ef7626b83008e08c22232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711602"
---
# <span data-ttu-id="0bed9-101">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="0bed9-101">Get-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="0bed9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bed9-102">SYNOPSIS</span></span>
<span data-ttu-id="0bed9-103">Azure Data Factory의 논리 게이트웨이에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0bed9-103">Gets information about logical gateways in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bed9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0bed9-104">SYNTAX</span></span>

### <span data-ttu-id="0bed9-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="0bed9-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bed9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0bed9-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bed9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0bed9-107">DESCRIPTION</span></span>
<span data-ttu-id="0bed9-108">**AzureRmDataFactoryGateway** Cmdlet은 Azure Data Factory의 논리 게이트웨이에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0bed9-108">The **Get-AzureRmDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="0bed9-109">게이트웨이의 이름을 지정 하는 경우이 cmdlet은 해당 게이트웨이에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0bed9-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="0bed9-110">이름을 지정 하지 않으면이 cmdlet은 data factory의 모든 게이트웨이에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0bed9-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>

<span data-ttu-id="0bed9-111">온-프레미스 Microsoft SQL Server를 data factory에 연결 된 서비스로 추가 하려면 온-프레미스 컴퓨터에 게이트웨이를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bed9-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="0bed9-112">예제의</span><span class="sxs-lookup"><span data-stu-id="0bed9-112">EXAMPLES</span></span>

### <span data-ttu-id="0bed9-113">예제 1: 데이터 팩터리에 모든 논리 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="0bed9-113">Example 1: Get all logical gateways in a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
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

<span data-ttu-id="0bed9-114">이 명령은 ADF 라는 리소스 그룹에 있는 WikiADF 이라는 data factory의 모든 논리 게이트웨이에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0bed9-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="0bed9-115">예제 2: 데이터 팩터리에 특정 논리 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="0bed9-115">Example 2: Get a specific logical gateway in a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "Gateway01" -DataFactoryName "WikiADF"
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

<span data-ttu-id="0bed9-116">이 명령은 ADF 라는 리소스 그룹의 WikiADF 이라는 data factory의 Gateway01 이라는 논리 게이트웨이에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0bed9-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="0bed9-117">변수</span><span class="sxs-lookup"><span data-stu-id="0bed9-117">PARAMETERS</span></span>

### <span data-ttu-id="0bed9-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0bed9-118">-DataFactory</span></span>
<span data-ttu-id="0bed9-119">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bed9-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="0bed9-120">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 논리 게이트웨이에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0bed9-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0bed9-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0bed9-121">-DataFactoryName</span></span>
<span data-ttu-id="0bed9-122">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bed9-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0bed9-123">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 논리 게이트웨이에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0bed9-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0bed9-124">-이름</span><span class="sxs-lookup"><span data-stu-id="0bed9-124">-Name</span></span>
<span data-ttu-id="0bed9-125">정보를 가져올 논리 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bed9-125">Specifies the name of the logical gateway about which to get information.</span></span>

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

### <span data-ttu-id="0bed9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bed9-126">-ResourceGroupName</span></span>
<span data-ttu-id="0bed9-127">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bed9-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0bed9-128">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 논리 게이트웨이에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0bed9-128">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0bed9-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bed9-129">-DefaultProfile</span></span>
<span data-ttu-id="0bed9-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0bed9-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bed9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bed9-131">CommonParameters</span></span>
<span data-ttu-id="0bed9-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bed9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bed9-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bed9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bed9-134">입력</span><span class="sxs-lookup"><span data-stu-id="0bed9-134">INPUTS</span></span>

## <span data-ttu-id="0bed9-135">출력</span><span class="sxs-lookup"><span data-stu-id="0bed9-135">OUTPUTS</span></span>

### <span data-ttu-id="0bed9-136">AtaFactoryGateway에서 ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSD]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bed9-136">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span></span>

## <span data-ttu-id="0bed9-137">상속자</span><span class="sxs-lookup"><span data-stu-id="0bed9-137">NOTES</span></span>
* <span data-ttu-id="0bed9-138">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="0bed9-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0bed9-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0bed9-139">RELATED LINKS</span></span>

[<span data-ttu-id="0bed9-140">새로운 AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="0bed9-140">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="0bed9-141">제거-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="0bed9-141">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="0bed9-142">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="0bed9-142">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


