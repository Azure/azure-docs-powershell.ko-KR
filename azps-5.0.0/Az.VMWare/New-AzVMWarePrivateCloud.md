---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
ms.openlocfilehash: 5dd91db9a8141bf9992da9eb364b00301036a898
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309378"
---
# <span data-ttu-id="d86e8-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="d86e8-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="d86e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d86e8-102">SYNOPSIS</span></span>
<span data-ttu-id="d86e8-103">사설 클라우드 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="d86e8-103">Create or update a private cloud</span></span>

## <span data-ttu-id="d86e8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d86e8-104">SYNTAX</span></span>

```
New-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d86e8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d86e8-105">DESCRIPTION</span></span>
<span data-ttu-id="d86e8-106">사설 클라우드 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="d86e8-106">Create or update a private cloud</span></span>

## <span data-ttu-id="d86e8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d86e8-107">EXAMPLES</span></span>

### <span data-ttu-id="d86e8-108">예제 1: 사설 클라우드 만들기</span><span class="sxs-lookup"><span data-stu-id="d86e8-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="d86e8-109">사설 클라우드 만들기</span><span class="sxs-lookup"><span data-stu-id="d86e8-109">Create private cloud</span></span>

## <span data-ttu-id="d86e8-110">변수</span><span class="sxs-lookup"><span data-stu-id="d86e8-110">PARAMETERS</span></span>

### <span data-ttu-id="d86e8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d86e8-111">-AsJob</span></span>
<span data-ttu-id="d86e8-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="d86e8-112">Run the command as a job</span></span>

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

### <span data-ttu-id="d86e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d86e8-113">-DefaultProfile</span></span>
<span data-ttu-id="d86e8-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d86e8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d86e8-115">-인터넷</span><span class="sxs-lookup"><span data-stu-id="d86e8-115">-Internet</span></span>
<span data-ttu-id="d86e8-116">인터넷 연결을 사용 하거나 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="d86e8-116">Connectivity to internet is enabled or disabled</span></span>

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

### <span data-ttu-id="d86e8-117">-위치</span><span class="sxs-lookup"><span data-stu-id="d86e8-117">-Location</span></span>
<span data-ttu-id="d86e8-118">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="d86e8-118">Resource location</span></span>

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

### <span data-ttu-id="d86e8-119">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="d86e8-119">-ManagementClusterSize</span></span>
<span data-ttu-id="d86e8-120">클러스터 크기</span><span class="sxs-lookup"><span data-stu-id="d86e8-120">The cluster size</span></span>

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

### <span data-ttu-id="d86e8-121">-이름</span><span class="sxs-lookup"><span data-stu-id="d86e8-121">-Name</span></span>
<span data-ttu-id="d86e8-122">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="d86e8-122">Name of the private cloud</span></span>

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

### <span data-ttu-id="d86e8-123">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="d86e8-123">-NetworkBlock</span></span>
<span data-ttu-id="d86e8-124">주소 블록은 구독 및 온-프레미스의 VNet에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d86e8-124">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="d86e8-125">A, B, C, D가 0과 255 사이에 있고 X가 0에서 22 사이인 CIDR 형식이 (A. b. .C/X)에 적용 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d86e8-125">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="d86e8-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d86e8-126">-NoWait</span></span>
<span data-ttu-id="d86e8-127">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="d86e8-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d86e8-128">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="d86e8-128">-NsxtPassword</span></span>
<span data-ttu-id="d86e8-129">필요에 따라 사설 클라우드가 생성 될 때 NSX Manager 암호를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d86e8-129">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="d86e8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d86e8-130">-ResourceGroupName</span></span>
<span data-ttu-id="d86e8-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d86e8-131">The name of the resource group.</span></span>
<span data-ttu-id="d86e8-132">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="d86e8-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d86e8-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="d86e8-133">-Sku</span></span>
<span data-ttu-id="d86e8-134">SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d86e8-134">The name of the SKU.</span></span>

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

### <span data-ttu-id="d86e8-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d86e8-135">-SubscriptionId</span></span>
<span data-ttu-id="d86e8-136">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d86e8-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d86e8-137">태그</span><span class="sxs-lookup"><span data-stu-id="d86e8-137">-Tag</span></span>
<span data-ttu-id="d86e8-138">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="d86e8-138">Resource tags</span></span>

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

### <span data-ttu-id="d86e8-139">-Vc비밀 번호</span><span class="sxs-lookup"><span data-stu-id="d86e8-139">-VcenterPassword</span></span>
<span data-ttu-id="d86e8-140">선택적으로 사설 클라우드가 생성 될 때 vCenter 관리자 암호를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d86e8-140">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="d86e8-141">-확인</span><span class="sxs-lookup"><span data-stu-id="d86e8-141">-Confirm</span></span>
<span data-ttu-id="d86e8-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d86e8-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d86e8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d86e8-143">-WhatIf</span></span>
<span data-ttu-id="d86e8-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d86e8-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d86e8-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d86e8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d86e8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d86e8-146">CommonParameters</span></span>
<span data-ttu-id="d86e8-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d86e8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d86e8-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d86e8-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d86e8-149">입력</span><span class="sxs-lookup"><span data-stu-id="d86e8-149">INPUTS</span></span>

## <span data-ttu-id="d86e8-150">출력</span><span class="sxs-lookup"><span data-stu-id="d86e8-150">OUTPUTS</span></span>

### <span data-ttu-id="d86e8-151">Api20200320. IPrivateCloud에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d86e8-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="d86e8-152">상속자</span><span class="sxs-lookup"><span data-stu-id="d86e8-152">NOTES</span></span>

<span data-ttu-id="d86e8-153">별칭과</span><span class="sxs-lookup"><span data-stu-id="d86e8-153">ALIASES</span></span>

## <span data-ttu-id="d86e8-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d86e8-154">RELATED LINKS</span></span>

