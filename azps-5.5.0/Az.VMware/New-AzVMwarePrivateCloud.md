---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.VMware/new-azVMwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
ms.openlocfilehash: 3e5e8fa4d098ce68899294a25866b4636c80878e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188729"
---
# <span data-ttu-id="d0b55-101">New-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="d0b55-101">New-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="d0b55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0b55-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b55-103">사설 클라우드 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="d0b55-103">Create or update a private cloud</span></span>

## <span data-ttu-id="d0b55-104">구문</span><span class="sxs-lookup"><span data-stu-id="d0b55-104">SYNTAX</span></span>

```
New-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>] [-AcceptEULA]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d0b55-105">설명</span><span class="sxs-lookup"><span data-stu-id="d0b55-105">DESCRIPTION</span></span>
<span data-ttu-id="d0b55-106">사설 클라우드 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="d0b55-106">Create or update a private cloud</span></span>

## <span data-ttu-id="d0b55-107">예제</span><span class="sxs-lookup"><span data-stu-id="d0b55-107">EXAMPLES</span></span>

### <span data-ttu-id="d0b55-108">예제 1: 사설 클라우드 만들기</span><span class="sxs-lookup"><span data-stu-id="d0b55-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMwarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="d0b55-109">사설 클라우드 만들기</span><span class="sxs-lookup"><span data-stu-id="d0b55-109">Create private cloud</span></span>

## <span data-ttu-id="d0b55-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0b55-110">PARAMETERS</span></span>

### <span data-ttu-id="d0b55-111">-AcceptEULA</span><span class="sxs-lookup"><span data-stu-id="d0b55-111">-AcceptEULA</span></span>
<span data-ttu-id="d0b55-112">AVS의 EULA에 동의하면 이 매개 변수가 제공되지 않은 법적 용어가 팝업됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0b55-112">Accept EULA of AVS, legal term will pop up without this parameter provided</span></span>

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

### <span data-ttu-id="d0b55-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0b55-113">-AsJob</span></span>
<span data-ttu-id="d0b55-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="d0b55-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d0b55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0b55-115">-DefaultProfile</span></span>
<span data-ttu-id="d0b55-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0b55-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0b55-117">-Internet</span><span class="sxs-lookup"><span data-stu-id="d0b55-117">-Internet</span></span>
<span data-ttu-id="d0b55-118">인터넷에 대한 연결이 설정되거나 사용되지 않도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0b55-118">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0b55-119">-Location</span><span class="sxs-lookup"><span data-stu-id="d0b55-119">-Location</span></span>
<span data-ttu-id="d0b55-120">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="d0b55-120">Resource location</span></span>

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

### <span data-ttu-id="d0b55-121">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="d0b55-121">-ManagementClusterSize</span></span>
<span data-ttu-id="d0b55-122">클러스터 크기</span><span class="sxs-lookup"><span data-stu-id="d0b55-122">The cluster size</span></span>

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

### <span data-ttu-id="d0b55-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d0b55-123">-Name</span></span>
<span data-ttu-id="d0b55-124">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="d0b55-124">Name of the private cloud</span></span>

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

### <span data-ttu-id="d0b55-125">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="d0b55-125">-NetworkBlock</span></span>
<span data-ttu-id="d0b55-126">주소 블록은 구독의 VNet과 모든 VNet에서 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0b55-126">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="d0b55-127">CIDR 형식이 (A.B.C.D/X)를 준수하는지 확인</span><span class="sxs-lookup"><span data-stu-id="d0b55-127">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="d0b55-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d0b55-128">-NoWait</span></span>
<span data-ttu-id="d0b55-129">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="d0b55-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d0b55-130">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="d0b55-130">-NsxtPassword</span></span>
<span data-ttu-id="d0b55-131">선택적으로 사설 클라우드를 만들 때 NSX-T Manager 암호를 설정</span><span class="sxs-lookup"><span data-stu-id="d0b55-131">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="d0b55-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0b55-132">-ResourceGroupName</span></span>
<span data-ttu-id="d0b55-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0b55-133">The name of the resource group.</span></span>
<span data-ttu-id="d0b55-134">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="d0b55-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d0b55-135">-Sku</span><span class="sxs-lookup"><span data-stu-id="d0b55-135">-Sku</span></span>
<span data-ttu-id="d0b55-136">SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0b55-136">The name of the SKU.</span></span>

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

### <span data-ttu-id="d0b55-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d0b55-137">-SubscriptionId</span></span>
<span data-ttu-id="d0b55-138">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d0b55-138">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d0b55-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="d0b55-139">-Tag</span></span>
<span data-ttu-id="d0b55-140">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="d0b55-140">Resource tags</span></span>

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

### <span data-ttu-id="d0b55-141">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="d0b55-141">-VcenterPassword</span></span>
<span data-ttu-id="d0b55-142">선택적으로 사설 클라우드를 만들 때 vCenter 관리자 암호를 설정</span><span class="sxs-lookup"><span data-stu-id="d0b55-142">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="d0b55-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0b55-143">-Confirm</span></span>
<span data-ttu-id="d0b55-144">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0b55-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0b55-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0b55-145">-WhatIf</span></span>
<span data-ttu-id="d0b55-146">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d0b55-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0b55-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0b55-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0b55-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b55-148">CommonParameters</span></span>
<span data-ttu-id="d0b55-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d0b55-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b55-150">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d0b55-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b55-151">입력</span><span class="sxs-lookup"><span data-stu-id="d0b55-151">INPUTS</span></span>

## <span data-ttu-id="d0b55-152">출력</span><span class="sxs-lookup"><span data-stu-id="d0b55-152">OUTPUTS</span></span>

### <span data-ttu-id="d0b55-153">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="d0b55-153">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="d0b55-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d0b55-154">NOTES</span></span>

<span data-ttu-id="d0b55-155">별칭</span><span class="sxs-lookup"><span data-stu-id="d0b55-155">ALIASES</span></span>

## <span data-ttu-id="d0b55-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0b55-156">RELATED LINKS</span></span>

