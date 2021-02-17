---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
ms.openlocfilehash: d6a748897b956759ad64056b0d9b83a6e82e91fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200380"
---
# <span data-ttu-id="5cdfa-101">New-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="5cdfa-101">New-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="5cdfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cdfa-102">SYNOPSIS</span></span>
<span data-ttu-id="5cdfa-103">DigitalTwinsInstance의 메타데이터를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-103">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="5cdfa-104">속성을 수정하는 일반적인 패턴은 DigitalTwinsInstance 및 보안 메타데이터를 검색한 다음 새 본문의 수정된 값과 결합하여 DigitalTwinsInstance를 업데이트하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-104">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="5cdfa-105">구문</span><span class="sxs-lookup"><span data-stu-id="5cdfa-105">SYNTAX</span></span>

### <span data-ttu-id="5cdfa-106">CreateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="5cdfa-106">CreateExpanded (Default)</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> -Location <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5cdfa-107">만들기</span><span class="sxs-lookup"><span data-stu-id="5cdfa-107">Create</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsCreate <IDigitalTwinsDescription> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5cdfa-108">설명</span><span class="sxs-lookup"><span data-stu-id="5cdfa-108">DESCRIPTION</span></span>
<span data-ttu-id="5cdfa-109">DigitalTwinsInstance의 메타데이터를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-109">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="5cdfa-110">속성을 수정하는 일반적인 패턴은 DigitalTwinsInstance 및 보안 메타데이터를 검색한 다음 새 본문의 수정된 값과 결합하여 DigitalTwinsInstance를 업데이트하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-110">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="5cdfa-111">예제</span><span class="sxs-lookup"><span data-stu-id="5cdfa-111">EXAMPLES</span></span>

### <span data-ttu-id="5cdfa-112">예제 1: 기본적으로 AzDigitalTwinsInstance를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-112">Example 1: Create an AzDigitalTwinsInstance by default.</span></span>
```powershell
PS C:\> New-AzDigitalTwinsInstance -ResourceGroupName youritest -ResourceName youriDigitalTwin -Location eastus

Location Name             SkuName Type
-------- ----             ------- ----
eastus   youriDigitalTwin S1      Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="5cdfa-113">기본적으로 AzDigitalTwinsInstance 만들기</span><span class="sxs-lookup"><span data-stu-id="5cdfa-113">Create an AzDigitalTwinsInstance by default</span></span>

### <span data-ttu-id="5cdfa-114">예제 2: AzDigitalTwins Object로 AzDigitalTwinsInstance 만들기</span><span class="sxs-lookup"><span data-stu-id="5cdfa-114">Example 2: Create an AzDigitalTwinsInstance by AzDigitalTwins Object.</span></span>
```powershell
PS C:\> $GetAzDigTwin = Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest01 -DigitalTwinsCreate $getAzdigitalTwins

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest01 Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="5cdfa-115">AzDigitalTwins 개체로 AzDigitalTwinsInstance 만들기</span><span class="sxs-lookup"><span data-stu-id="5cdfa-115">Create an AzDigitalTwinsInstance by AzDigitalTwins Object</span></span>

## <span data-ttu-id="5cdfa-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cdfa-116">PARAMETERS</span></span>

### <span data-ttu-id="5cdfa-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5cdfa-117">-AsJob</span></span>
<span data-ttu-id="5cdfa-118">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="5cdfa-118">Run the command as a job</span></span>

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

### <span data-ttu-id="5cdfa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cdfa-119">-DefaultProfile</span></span>
<span data-ttu-id="5cdfa-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cdfa-121">-DigitalTwinsCreate</span><span class="sxs-lookup"><span data-stu-id="5cdfa-121">-DigitalTwinsCreate</span></span>
<span data-ttu-id="5cdfa-122">DigitalTwins 서비스에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-122">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="5cdfa-123">생성을 위해 DIGITALTWINSCREATE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-123">To construct, see NOTES section for DIGITALTWINSCREATE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cdfa-124">-Location</span><span class="sxs-lookup"><span data-stu-id="5cdfa-124">-Location</span></span>
<span data-ttu-id="5cdfa-125">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-125">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cdfa-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5cdfa-126">-NoWait</span></span>
<span data-ttu-id="5cdfa-127">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="5cdfa-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5cdfa-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cdfa-128">-ResourceGroupName</span></span>
<span data-ttu-id="5cdfa-129">DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-129">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="5cdfa-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5cdfa-130">-ResourceName</span></span>
<span data-ttu-id="5cdfa-131">DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-131">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="5cdfa-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5cdfa-132">-SubscriptionId</span></span>
<span data-ttu-id="5cdfa-133">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-133">The subscription identifier.</span></span>

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

### <span data-ttu-id="5cdfa-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="5cdfa-134">-Tag</span></span>
<span data-ttu-id="5cdfa-135">리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-135">The resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cdfa-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cdfa-136">-Confirm</span></span>
<span data-ttu-id="5cdfa-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cdfa-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cdfa-138">-WhatIf</span></span>
<span data-ttu-id="5cdfa-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5cdfa-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cdfa-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cdfa-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cdfa-141">CommonParameters</span></span>
<span data-ttu-id="5cdfa-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cdfa-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cdfa-144">입력</span><span class="sxs-lookup"><span data-stu-id="5cdfa-144">INPUTS</span></span>

### <span data-ttu-id="5cdfa-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="5cdfa-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="5cdfa-146">출력</span><span class="sxs-lookup"><span data-stu-id="5cdfa-146">OUTPUTS</span></span>

### <span data-ttu-id="5cdfa-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="5cdfa-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="5cdfa-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5cdfa-148">NOTES</span></span>

<span data-ttu-id="5cdfa-149">별칭</span><span class="sxs-lookup"><span data-stu-id="5cdfa-149">ALIASES</span></span>

<span data-ttu-id="5cdfa-150">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="5cdfa-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5cdfa-151">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5cdfa-152">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5cdfa-153">DIGITALTWINSCREATE: <IDigitalTwinsDescription> DigitalTwins 서비스에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-153">DIGITALTWINSCREATE <IDigitalTwinsDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="5cdfa-154">`Location <String>`: 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-154">`Location <String>`: The resource location.</span></span>
  - <span data-ttu-id="5cdfa-155">`[Tag <IDigitalTwinsResourceTags>]`: 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-155">`[Tag <IDigitalTwinsResourceTags>]`: The resource tags.</span></span>
    - <span data-ttu-id="5cdfa-156">`[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="5cdfa-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5cdfa-157">RELATED LINKS</span></span>

