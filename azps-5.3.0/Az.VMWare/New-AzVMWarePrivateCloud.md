---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
ms.openlocfilehash: 5dd91db9a8141bf9992da9eb364b00301036a898
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491506"
---
# <span data-ttu-id="5fe56-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="5fe56-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="5fe56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fe56-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe56-103">사설 클라우드 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="5fe56-103">Create or update a private cloud</span></span>

## <span data-ttu-id="5fe56-104">구문</span><span class="sxs-lookup"><span data-stu-id="5fe56-104">SYNTAX</span></span>

```
New-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5fe56-105">설명</span><span class="sxs-lookup"><span data-stu-id="5fe56-105">DESCRIPTION</span></span>
<span data-ttu-id="5fe56-106">사설 클라우드 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="5fe56-106">Create or update a private cloud</span></span>

## <span data-ttu-id="5fe56-107">예제</span><span class="sxs-lookup"><span data-stu-id="5fe56-107">EXAMPLES</span></span>

### <span data-ttu-id="5fe56-108">예제 1: 사설 클라우드 만들기</span><span class="sxs-lookup"><span data-stu-id="5fe56-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="5fe56-109">사설 클라우드 만들기</span><span class="sxs-lookup"><span data-stu-id="5fe56-109">Create private cloud</span></span>

## <span data-ttu-id="5fe56-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fe56-110">PARAMETERS</span></span>

### <span data-ttu-id="5fe56-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fe56-111">-AsJob</span></span>
<span data-ttu-id="5fe56-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="5fe56-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe56-113">-DefaultProfile</span></span>
<span data-ttu-id="5fe56-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5fe56-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fe56-115">-Internet</span><span class="sxs-lookup"><span data-stu-id="5fe56-115">-Internet</span></span>
<span data-ttu-id="5fe56-116">인터넷에 대한 연결이 설정되거나 사용되지 않도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5fe56-116">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe56-117">-Location</span><span class="sxs-lookup"><span data-stu-id="5fe56-117">-Location</span></span>
<span data-ttu-id="5fe56-118">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="5fe56-118">Resource location</span></span>

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

### <span data-ttu-id="5fe56-119">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="5fe56-119">-ManagementClusterSize</span></span>
<span data-ttu-id="5fe56-120">클러스터 크기</span><span class="sxs-lookup"><span data-stu-id="5fe56-120">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe56-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5fe56-121">-Name</span></span>
<span data-ttu-id="5fe56-122">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="5fe56-122">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe56-123">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="5fe56-123">-NetworkBlock</span></span>
<span data-ttu-id="5fe56-124">주소 블록은 구독의 VNet과 모든 VNet에서 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe56-124">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="5fe56-125">CIDR 형식이 (A.B.C.D/X)를 준수하는지 확인</span><span class="sxs-lookup"><span data-stu-id="5fe56-125">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="5fe56-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5fe56-126">-NoWait</span></span>
<span data-ttu-id="5fe56-127">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="5fe56-127">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe56-128">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="5fe56-128">-NsxtPassword</span></span>
<span data-ttu-id="5fe56-129">선택적으로 사설 클라우드를 만들 때 NSX-T Manager 암호를 설정</span><span class="sxs-lookup"><span data-stu-id="5fe56-129">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe56-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fe56-130">-ResourceGroupName</span></span>
<span data-ttu-id="5fe56-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5fe56-131">The name of the resource group.</span></span>
<span data-ttu-id="5fe56-132">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe56-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5fe56-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="5fe56-133">-Sku</span></span>
<span data-ttu-id="5fe56-134">SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5fe56-134">The name of the SKU.</span></span>

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

### <span data-ttu-id="5fe56-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5fe56-135">-SubscriptionId</span></span>
<span data-ttu-id="5fe56-136">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5fe56-136">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe56-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="5fe56-137">-Tag</span></span>
<span data-ttu-id="5fe56-138">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="5fe56-138">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe56-139">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="5fe56-139">-VcenterPassword</span></span>
<span data-ttu-id="5fe56-140">선택적으로 사설 클라우드를 만들 때 vCenter 관리자 암호를 설정</span><span class="sxs-lookup"><span data-stu-id="5fe56-140">Optionally, set the vCenter admin password when the private cloud is created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe56-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fe56-141">-Confirm</span></span>
<span data-ttu-id="5fe56-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5fe56-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe56-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fe56-143">-WhatIf</span></span>
<span data-ttu-id="5fe56-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5fe56-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fe56-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5fe56-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe56-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe56-146">CommonParameters</span></span>
<span data-ttu-id="5fe56-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe56-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe56-148">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5fe56-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe56-149">입력</span><span class="sxs-lookup"><span data-stu-id="5fe56-149">INPUTS</span></span>

## <span data-ttu-id="5fe56-150">출력</span><span class="sxs-lookup"><span data-stu-id="5fe56-150">OUTPUTS</span></span>

### <span data-ttu-id="5fe56-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="5fe56-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="5fe56-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5fe56-152">NOTES</span></span>

<span data-ttu-id="5fe56-153">별칭</span><span class="sxs-lookup"><span data-stu-id="5fe56-153">ALIASES</span></span>

## <span data-ttu-id="5fe56-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5fe56-154">RELATED LINKS</span></span>

