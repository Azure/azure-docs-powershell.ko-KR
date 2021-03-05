---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
ms.openlocfilehash: 3d3d8e5cd7855e03d5f02ddaee6b38c98aeacb0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008064"
---
# <span data-ttu-id="0b8be-101">Get-AzCloudServiceRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="0b8be-101">Get-AzCloudServiceRoleInstanceView</span></span>

## <span data-ttu-id="0b8be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b8be-102">SYNOPSIS</span></span>
<span data-ttu-id="0b8be-103">클라우드 서비스의 역할 인스턴스의 런타시 상태 정보를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="0b8be-103">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="0b8be-104">구문</span><span class="sxs-lookup"><span data-stu-id="0b8be-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0b8be-105">설명</span><span class="sxs-lookup"><span data-stu-id="0b8be-105">DESCRIPTION</span></span>
<span data-ttu-id="0b8be-106">클라우드 서비스의 역할 인스턴스의 런타시 상태 정보를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="0b8be-106">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="0b8be-107">예제</span><span class="sxs-lookup"><span data-stu-id="0b8be-107">EXAMPLES</span></span>

### <span data-ttu-id="0b8be-108">예제 1: 클라우드 서비스 역할 인스턴스에 대한 인스턴스 보기 세부 정보 보기 보기</span><span class="sxs-lookup"><span data-stu-id="0b8be-108">Example 1: Get instance view details for cloud service role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Statuses           PlatformFaultDomain PlatformUpdateDomain
--------           ------------------- --------------------
{RoleStateStarted} 0                   0

```

<span data-ttu-id="0b8be-109">이 cmdlet은 ContosOrg라는 리소스 그룹에 ContosoFrontEnd_IN_0 ContosoCS라는 클라우드 서비스의 역할 인스턴스의 인스턴스 보기를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0b8be-109">This cmdlet gets the instance view of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="0b8be-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0b8be-110">PARAMETERS</span></span>

### <span data-ttu-id="0b8be-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="0b8be-111">-CloudServiceName</span></span>
<span data-ttu-id="0b8be-112">.</span><span class="sxs-lookup"><span data-stu-id="0b8be-112">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b8be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b8be-113">-DefaultProfile</span></span>
<span data-ttu-id="0b8be-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0b8be-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b8be-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b8be-115">-ResourceGroupName</span></span>
<span data-ttu-id="0b8be-116">.</span><span class="sxs-lookup"><span data-stu-id="0b8be-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b8be-117">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="0b8be-117">-RoleInstanceName</span></span>
<span data-ttu-id="0b8be-118">역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b8be-118">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b8be-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b8be-119">-SubscriptionId</span></span>
<span data-ttu-id="0b8be-120">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="0b8be-120">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0b8be-121">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="0b8be-121">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b8be-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b8be-122">CommonParameters</span></span>
<span data-ttu-id="0b8be-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0b8be-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b8be-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b8be-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b8be-125">입력</span><span class="sxs-lookup"><span data-stu-id="0b8be-125">INPUTS</span></span>

## <span data-ttu-id="0b8be-126">출력</span><span class="sxs-lookup"><span data-stu-id="0b8be-126">OUTPUTS</span></span>

### <span data-ttu-id="0b8be-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="0b8be-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span></span>

## <span data-ttu-id="0b8be-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0b8be-128">NOTES</span></span>

<span data-ttu-id="0b8be-129">별칭</span><span class="sxs-lookup"><span data-stu-id="0b8be-129">ALIASES</span></span>

## <span data-ttu-id="0b8be-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b8be-130">RELATED LINKS</span></span>

