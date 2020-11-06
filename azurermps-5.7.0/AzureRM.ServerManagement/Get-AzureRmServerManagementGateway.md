---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: C579BF90-FD8B-4384-96EB-46154E308492
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/get-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
ms.openlocfilehash: 9dc7e38cf169e79ec7dae279c6fa09f069b1ade7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524932"
---
# <span data-ttu-id="742eb-101">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="742eb-101">Get-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="742eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="742eb-102">SYNOPSIS</span></span>
<span data-ttu-id="742eb-103">하나 이상의 서버 관리 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="742eb-103">Gets one or more Server Management Gateways.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="742eb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="742eb-104">SYNTAX</span></span>

### <span data-ttu-id="742eb-105">NoParams (기본값)</span><span class="sxs-lookup"><span data-stu-id="742eb-105">NoParams (Default)</span></span>
```
Get-AzureRmServerManagementGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="742eb-106">Many-ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="742eb-106">Many-ByResourceGroup</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="742eb-107">Single-ByName</span><span class="sxs-lookup"><span data-stu-id="742eb-107">Single-ByName</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="742eb-108">Single-ByObject</span><span class="sxs-lookup"><span data-stu-id="742eb-108">Single-ByObject</span></span>
```
Get-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="742eb-109">설명은</span><span class="sxs-lookup"><span data-stu-id="742eb-109">DESCRIPTION</span></span>
<span data-ttu-id="742eb-110">**AzureRmServerManagementGateway** cmdlet은 하나 이상의 Azure 서버 관리 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="742eb-110">The **Get-AzureRmServerManagementGateway** cmdlet gets one or more Azure Server Management Gateways.</span></span>

## <span data-ttu-id="742eb-111">예제의</span><span class="sxs-lookup"><span data-stu-id="742eb-111">EXAMPLES</span></span>

### <span data-ttu-id="742eb-112">예제 1: 구독에 있는 모든 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="742eb-112">Example 1: Get all gateways in a subscription</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
groupOne       centralus      Off          mygateway
groupOne       centralus      Off          othergateway
groupTwo       centralus      On           privategateway
```

<span data-ttu-id="742eb-113">이 명령은 구독에 있는 모든 서버 관리 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="742eb-113">This command gets all Server Management Gateways in the subscription.</span></span>

### <span data-ttu-id="742eb-114">예제 2: 리소스 그룹에서 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="742eb-114">Example 2: Get gateways in a resource group</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway -ResourceGroupName "Group001"
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
myGroup        centralus      Off          mygateway
```

<span data-ttu-id="742eb-115">이 명령은 Group001 이라는 리소스 그룹에 속하는 모든 서버 관리 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="742eb-115">This command gets all Server Management Gateways that belong to the resource group named Group001.</span></span>

### <span data-ttu-id="742eb-116">예제 3: 설치 된 게이트웨이의 모든 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="742eb-116">Example 3: Get all installed instances of a gateway</span></span>
```
PS C:\>(Get-AzureRmServerManagementGateway -ResourceGroupName "Group002" -GatewayName "Gateway01").Instances
Name             Installed              Version         Operating System
----             ---------              -------         ----------------
GATEWAYPC        4/13/2016 6:35:04 PM   1.0.1104.0      Microsoft Windows 10 Enterprise
```

<span data-ttu-id="742eb-117">이 명령은 Group002 이라는 리소스 그룹에 속하는 Gateway01 이라는 서버 관리 게이트웨이의 모든 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="742eb-117">This command gets all instances of a Server Management Gateway named Gateway01 that belong to the resource group named Group002.</span></span>

## <span data-ttu-id="742eb-118">변수</span><span class="sxs-lookup"><span data-stu-id="742eb-118">PARAMETERS</span></span>

### <span data-ttu-id="742eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="742eb-119">-DefaultProfile</span></span>
<span data-ttu-id="742eb-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="742eb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="742eb-121">-게이트웨이</span><span class="sxs-lookup"><span data-stu-id="742eb-121">-Gateway</span></span>
<span data-ttu-id="742eb-122">이 cmdlet이 가져오는 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="742eb-122">Specifies a gateway that this cmdlet gets.</span></span>

<span data-ttu-id="742eb-123">Cmdlet은 지정 된 게이트웨이를 통해 *ResourceGroupName* 및 *게이트웨이 이름* 매개 변수를 사용 하 여 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="742eb-123">The cmdlet uses the *ResourceGroupName* and *GatewayName* parameters through the specified Gateway to perform the action.</span></span>

<span data-ttu-id="742eb-124">이 매개 변수를 지정 하면이 cmdlet에는 게이트웨이에 대 한 자세한 상태가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="742eb-124">When this parameter is specified, this cmdlet will include detailed status for the gateway.</span></span>

```yaml
Type: Gateway
Parameter Sets: Single-ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="742eb-125">--게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="742eb-125">-GatewayName</span></span>
<span data-ttu-id="742eb-126">이 cmdlet이 게이트를 가져오는 서버 관리 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="742eb-126">Specifies the name of the Server Management Gateway for which this cmdlet gets gate.</span></span>

<span data-ttu-id="742eb-127">않아도 *name* 매개 변수를 지정 하면이 cmdlet에는 게이트웨이에 대 한 자세한 상태가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="742eb-127">When you specify the *GatewayName* parameter, this cmdlet will include detailed status on the gateway.</span></span>

```yaml
Type: String
Parameter Sets: Single-ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742eb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="742eb-128">-ResourceGroupName</span></span>
<span data-ttu-id="742eb-129">이 cmdlet이 게이트웨이를 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="742eb-129">Specifies the name of the resource group for which this cmdlet gets gateways.</span></span>

```yaml
Type: String
Parameter Sets: Many-ByResourceGroup, Single-ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742eb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="742eb-130">CommonParameters</span></span>
<span data-ttu-id="742eb-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="742eb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="742eb-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="742eb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="742eb-133">입력</span><span class="sxs-lookup"><span data-stu-id="742eb-133">INPUTS</span></span>

### <span data-ttu-id="742eb-134">게이트웨이와</span><span class="sxs-lookup"><span data-stu-id="742eb-134">Gateway</span></span>
<span data-ttu-id="742eb-135">' Gateway ' 매개 변수는 파이프라인에서 ' Gateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="742eb-135">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="742eb-136">출력</span><span class="sxs-lookup"><span data-stu-id="742eb-136">OUTPUTS</span></span>

### <span data-ttu-id="742eb-137">Microsoft. ServerManagement. 모델 게이트웨이</span><span class="sxs-lookup"><span data-stu-id="742eb-137">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="742eb-138">상속자</span><span class="sxs-lookup"><span data-stu-id="742eb-138">NOTES</span></span>
* <span data-ttu-id="742eb-139">매개 변수 없이이 cmdlet을 사용 하는 경우 구독과 연결 된 모든 게이트웨이가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="742eb-139">If this cmdlet is use without parameters, it will return all the gateways associated with the subscription.</span></span>

## <span data-ttu-id="742eb-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="742eb-140">RELATED LINKS</span></span>

[<span data-ttu-id="742eb-141">새로운 AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="742eb-141">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)

[<span data-ttu-id="742eb-142">제거-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="742eb-142">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


