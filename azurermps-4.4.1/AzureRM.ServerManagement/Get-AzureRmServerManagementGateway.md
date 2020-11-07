---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: C579BF90-FD8B-4384-96EB-46154E308492
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
ms.openlocfilehash: 6b98f4266e730e1cfb60ef51046e6846f24999d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702691"
---
# <span data-ttu-id="70f83-101">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="70f83-101">Get-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="70f83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70f83-102">SYNOPSIS</span></span>
<span data-ttu-id="70f83-103">하나 이상의 서버 관리 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70f83-103">Gets one or more Server Management Gateways.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70f83-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70f83-104">SYNTAX</span></span>

### <span data-ttu-id="70f83-105">NoParams (기본값)</span><span class="sxs-lookup"><span data-stu-id="70f83-105">NoParams (Default)</span></span>
```
Get-AzureRmServerManagementGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70f83-106">Many-ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="70f83-106">Many-ByResourceGroup</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="70f83-107">Single-ByName</span><span class="sxs-lookup"><span data-stu-id="70f83-107">Single-ByName</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70f83-108">Single-ByObject</span><span class="sxs-lookup"><span data-stu-id="70f83-108">Single-ByObject</span></span>
```
Get-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70f83-109">설명은</span><span class="sxs-lookup"><span data-stu-id="70f83-109">DESCRIPTION</span></span>
<span data-ttu-id="70f83-110">**AzureRmServerManagementGateway** cmdlet은 하나 이상의 Azure 서버 관리 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70f83-110">The **Get-AzureRmServerManagementGateway** cmdlet gets one or more Azure Server Management Gateways.</span></span>

## <span data-ttu-id="70f83-111">예제의</span><span class="sxs-lookup"><span data-stu-id="70f83-111">EXAMPLES</span></span>

### <span data-ttu-id="70f83-112">예제 1: 구독에 있는 모든 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="70f83-112">Example 1: Get all gateways in a subscription</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
groupOne       centralus      Off          mygateway
groupOne       centralus      Off          othergateway
groupTwo       centralus      On           privategateway
```

<span data-ttu-id="70f83-113">이 명령은 구독에 있는 모든 서버 관리 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70f83-113">This command gets all Server Management Gateways in the subscription.</span></span>

### <span data-ttu-id="70f83-114">예제 2: 리소스 그룹에서 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="70f83-114">Example 2: Get gateways in a resource group</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway -ResourceGroupName "Group001"
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
myGroup        centralus      Off          mygateway
```

<span data-ttu-id="70f83-115">이 명령은 Group001 이라는 리소스 그룹에 속하는 모든 서버 관리 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70f83-115">This command gets all Server Management Gateways that belong to the resource group named Group001.</span></span>

### <span data-ttu-id="70f83-116">예제 3: 설치 된 게이트웨이의 모든 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="70f83-116">Example 3: Get all installed instances of a gateway</span></span>
```
PS C:\>(Get-AzureRmServerManagementGateway -ResourceGroupName "Group002" -GatewayName "Gateway01").Instances
Name             Installed              Version         Operating System
----             ---------              -------         ----------------
GATEWAYPC        4/13/2016 6:35:04 PM   1.0.1104.0      Microsoft Windows 10 Enterprise
```

<span data-ttu-id="70f83-117">이 명령은 Group002 이라는 리소스 그룹에 속하는 Gateway01 이라는 서버 관리 게이트웨이의 모든 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70f83-117">This command gets all instances of a Server Management Gateway named Gateway01 that belong to the resource group named Group002.</span></span>

## <span data-ttu-id="70f83-118">변수</span><span class="sxs-lookup"><span data-stu-id="70f83-118">PARAMETERS</span></span>

### <span data-ttu-id="70f83-119">-게이트웨이</span><span class="sxs-lookup"><span data-stu-id="70f83-119">-Gateway</span></span>
<span data-ttu-id="70f83-120">이 cmdlet이 가져오는 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70f83-120">Specifies a gateway that this cmdlet gets.</span></span>

<span data-ttu-id="70f83-121">Cmdlet은 지정 된 게이트웨이를 통해 *ResourceGroupName* 및 *게이트웨이 이름* 매개 변수를 사용 하 여 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="70f83-121">The cmdlet uses the *ResourceGroupName* and *GatewayName* parameters through the specified Gateway to perform the action.</span></span>

<span data-ttu-id="70f83-122">이 매개 변수를 지정 하면이 cmdlet에는 게이트웨이에 대 한 자세한 상태가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70f83-122">When this parameter is specified, this cmdlet will include detailed status for the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: Single-ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70f83-123">--게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="70f83-123">-GatewayName</span></span>
<span data-ttu-id="70f83-124">이 cmdlet이 게이트를 가져오는 서버 관리 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70f83-124">Specifies the name of the Server Management Gateway for which this cmdlet gets gate.</span></span>

<span data-ttu-id="70f83-125">않아도 *name* 매개 변수를 지정 하면이 cmdlet에는 게이트웨이에 대 한 자세한 상태가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70f83-125">When you specify the *GatewayName* parameter, this cmdlet will include detailed status on the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: Single-ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f83-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70f83-126">-ResourceGroupName</span></span>
<span data-ttu-id="70f83-127">이 cmdlet이 게이트웨이를 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70f83-127">Specifies the name of the resource group for which this cmdlet gets gateways.</span></span>

```yaml
Type: System.String
Parameter Sets: Many-ByResourceGroup, Single-ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f83-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f83-128">-DefaultProfile</span></span>
<span data-ttu-id="70f83-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70f83-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70f83-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f83-130">CommonParameters</span></span>
<span data-ttu-id="70f83-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70f83-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f83-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70f83-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f83-133">입력</span><span class="sxs-lookup"><span data-stu-id="70f83-133">INPUTS</span></span>

### <span data-ttu-id="70f83-134">게이트웨이와</span><span class="sxs-lookup"><span data-stu-id="70f83-134">Gateway</span></span>
<span data-ttu-id="70f83-135">' Gateway ' 매개 변수는 파이프라인에서 ' Gateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="70f83-135">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="70f83-136">출력</span><span class="sxs-lookup"><span data-stu-id="70f83-136">OUTPUTS</span></span>

### <span data-ttu-id="70f83-137">Microsoft. ServerManagement. 모델 게이트웨이</span><span class="sxs-lookup"><span data-stu-id="70f83-137">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="70f83-138">상속자</span><span class="sxs-lookup"><span data-stu-id="70f83-138">NOTES</span></span>
* <span data-ttu-id="70f83-139">매개 변수 없이이 cmdlet을 사용 하는 경우 구독과 연결 된 모든 게이트웨이가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70f83-139">If this cmdlet is use without parameters, it will return all the gateways associated with the subscription.</span></span>

## <span data-ttu-id="70f83-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70f83-140">RELATED LINKS</span></span>

[<span data-ttu-id="70f83-141">새로운 AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="70f83-141">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)

[<span data-ttu-id="70f83-142">제거-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="70f83-142">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


