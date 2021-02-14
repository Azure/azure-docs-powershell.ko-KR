---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
ms.openlocfilehash: a86ebbda321f37a38b3d014377081087f37feb9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181793"
---
# <span data-ttu-id="d5994-101">Get-AzCloudServiceRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="d5994-101">Get-AzCloudServiceRoleInstanceView</span></span>

## <span data-ttu-id="d5994-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5994-102">SYNOPSIS</span></span>
<span data-ttu-id="d5994-103">클라우드 서비스에서 역할 인스턴스의 런타시 상태 정보를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="d5994-103">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="d5994-104">구문</span><span class="sxs-lookup"><span data-stu-id="d5994-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d5994-105">설명</span><span class="sxs-lookup"><span data-stu-id="d5994-105">DESCRIPTION</span></span>
<span data-ttu-id="d5994-106">클라우드 서비스에서 역할 인스턴스의 런타시 상태 정보를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="d5994-106">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="d5994-107">예제</span><span class="sxs-lookup"><span data-stu-id="d5994-107">EXAMPLES</span></span>

### <span data-ttu-id="d5994-108">예제 1: 클라우드 서비스 역할 인스턴스에 대한 인스턴스 보기 세부 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="d5994-108">Example 1: Get instance view details for cloud service role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Statuses           PlatformFaultDomain PlatformUpdateDomain
--------           ------------------- --------------------
{RoleStateStarted} 0                   0

```

<span data-ttu-id="d5994-109">이 cmdlet은 ContosOrg라는 리소스 그룹에 속한 ContosoCS라는 ContosoFrontEnd_IN_0 서비스 이름의 역할 인스턴스의 인스턴스 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d5994-109">This cmdlet gets the instance view of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="d5994-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5994-110">PARAMETERS</span></span>

### <span data-ttu-id="d5994-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="d5994-111">-CloudServiceName</span></span>
<span data-ttu-id="d5994-112">.</span><span class="sxs-lookup"><span data-stu-id="d5994-112">.</span></span>

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

### <span data-ttu-id="d5994-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5994-113">-DefaultProfile</span></span>
<span data-ttu-id="d5994-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5994-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5994-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5994-115">-ResourceGroupName</span></span>
<span data-ttu-id="d5994-116">.</span><span class="sxs-lookup"><span data-stu-id="d5994-116">.</span></span>

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

### <span data-ttu-id="d5994-117">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="d5994-117">-RoleInstanceName</span></span>
<span data-ttu-id="d5994-118">역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5994-118">Name of the role instance.</span></span>

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

### <span data-ttu-id="d5994-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5994-119">-SubscriptionId</span></span>
<span data-ttu-id="d5994-120">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="d5994-120">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d5994-121">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="d5994-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d5994-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5994-122">CommonParameters</span></span>
<span data-ttu-id="d5994-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d5994-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5994-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d5994-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5994-125">입력</span><span class="sxs-lookup"><span data-stu-id="d5994-125">INPUTS</span></span>

## <span data-ttu-id="d5994-126">출력</span><span class="sxs-lookup"><span data-stu-id="d5994-126">OUTPUTS</span></span>

### <span data-ttu-id="d5994-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="d5994-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span></span>

## <span data-ttu-id="d5994-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d5994-128">NOTES</span></span>

<span data-ttu-id="d5994-129">별칭</span><span class="sxs-lookup"><span data-stu-id="d5994-129">ALIASES</span></span>

## <span data-ttu-id="d5994-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5994-130">RELATED LINKS</span></span>

