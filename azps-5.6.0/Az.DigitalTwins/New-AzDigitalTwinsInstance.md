---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/new-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
ms.openlocfilehash: 54fdbcfe83dd93101030d92f9f3eec19d1a2564f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984937"
---
# <span data-ttu-id="a186d-101">New-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="a186d-101">New-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="a186d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a186d-102">SYNOPSIS</span></span>
<span data-ttu-id="a186d-103">DigitalTwinsInstance의 메타데이터를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-103">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="a186d-104">속성을 수정하는 일반적인 패턴은 DigitalTwinsInstance 및 보안 메타데이터를 검색한 다음 새 본문의 수정된 값과 결합하여 DigitalTwinsInstance를 업데이트하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-104">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="a186d-105">구문</span><span class="sxs-lookup"><span data-stu-id="a186d-105">SYNTAX</span></span>

### <span data-ttu-id="a186d-106">CreateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="a186d-106">CreateExpanded (Default)</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> -Location <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a186d-107">만들기</span><span class="sxs-lookup"><span data-stu-id="a186d-107">Create</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsCreate <IDigitalTwinsDescription> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a186d-108">설명</span><span class="sxs-lookup"><span data-stu-id="a186d-108">DESCRIPTION</span></span>
<span data-ttu-id="a186d-109">DigitalTwinsInstance의 메타데이터를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-109">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="a186d-110">속성을 수정하는 일반적인 패턴은 DigitalTwinsInstance 및 보안 메타데이터를 검색한 다음 새 본문의 수정된 값과 결합하여 DigitalTwinsInstance를 업데이트하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-110">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="a186d-111">예제</span><span class="sxs-lookup"><span data-stu-id="a186d-111">EXAMPLES</span></span>

### <span data-ttu-id="a186d-112">예제 1: 기본적으로 AzDigitalTwinsInstance 만들기</span><span class="sxs-lookup"><span data-stu-id="a186d-112">Example 1: Create an AzDigitalTwinsInstance by default.</span></span>
```powershell
PS C:\> New-AzDigitalTwinsInstance -ResourceGroupName youritest -ResourceName youriDigitalTwin -Location eastus

Location Name             SkuName Type
-------- ----             ------- ----
eastus   youriDigitalTwin S1      Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="a186d-113">기본적으로 AzDigitalTwinsInstance 만들기</span><span class="sxs-lookup"><span data-stu-id="a186d-113">Create an AzDigitalTwinsInstance by default</span></span>

### <span data-ttu-id="a186d-114">예제 2: AzDigitalTwins 개체에 의해 AzDigitalTwinsInstance 만들기</span><span class="sxs-lookup"><span data-stu-id="a186d-114">Example 2: Create an AzDigitalTwinsInstance by AzDigitalTwins Object.</span></span>
```powershell
PS C:\> $GetAzDigTwin = Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest01 -DigitalTwinsCreate $getAzdigitalTwins

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest01 Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="a186d-115">AzDigitalTwinsInstance by AzDigitalTwins 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="a186d-115">Create an AzDigitalTwinsInstance by AzDigitalTwins Object</span></span>

## <span data-ttu-id="a186d-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a186d-116">PARAMETERS</span></span>

### <span data-ttu-id="a186d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a186d-117">-AsJob</span></span>
<span data-ttu-id="a186d-118">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-118">Run the command as a job</span></span>

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

### <span data-ttu-id="a186d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a186d-119">-DefaultProfile</span></span>
<span data-ttu-id="a186d-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a186d-121">-DigitalTwinsCreate</span><span class="sxs-lookup"><span data-stu-id="a186d-121">-DigitalTwinsCreate</span></span>
<span data-ttu-id="a186d-122">DigitalTwins 서비스에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-122">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="a186d-123">생성을 위해 DIGITALTWINSCREATE 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="a186d-123">To construct, see NOTES section for DIGITALTWINSCREATE properties and create a hash table.</span></span>

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

### <span data-ttu-id="a186d-124">-Location</span><span class="sxs-lookup"><span data-stu-id="a186d-124">-Location</span></span>
<span data-ttu-id="a186d-125">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-125">The resource location.</span></span>

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

### <span data-ttu-id="a186d-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a186d-126">-NoWait</span></span>
<span data-ttu-id="a186d-127">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="a186d-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a186d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a186d-128">-ResourceGroupName</span></span>
<span data-ttu-id="a186d-129">DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-129">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="a186d-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a186d-130">-ResourceName</span></span>
<span data-ttu-id="a186d-131">DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-131">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="a186d-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a186d-132">-SubscriptionId</span></span>
<span data-ttu-id="a186d-133">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-133">The subscription identifier.</span></span>

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

### <span data-ttu-id="a186d-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="a186d-134">-Tag</span></span>
<span data-ttu-id="a186d-135">리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-135">The resource tags.</span></span>

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

### <span data-ttu-id="a186d-136">-확인</span><span class="sxs-lookup"><span data-stu-id="a186d-136">-Confirm</span></span>
<span data-ttu-id="a186d-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a186d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a186d-138">-WhatIf</span></span>
<span data-ttu-id="a186d-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a186d-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a186d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a186d-141">CommonParameters</span></span>
<span data-ttu-id="a186d-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a186d-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a186d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a186d-144">입력</span><span class="sxs-lookup"><span data-stu-id="a186d-144">INPUTS</span></span>

### <span data-ttu-id="a186d-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="a186d-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="a186d-146">출력</span><span class="sxs-lookup"><span data-stu-id="a186d-146">OUTPUTS</span></span>

### <span data-ttu-id="a186d-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="a186d-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="a186d-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a186d-148">NOTES</span></span>

<span data-ttu-id="a186d-149">별칭</span><span class="sxs-lookup"><span data-stu-id="a186d-149">ALIASES</span></span>

<span data-ttu-id="a186d-150">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a186d-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a186d-151">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a186d-152">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a186d-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a186d-153">DIGITALTWINSCREATE <IDigitalTwinsDescription> : DigitalTwins 서비스에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-153">DIGITALTWINSCREATE <IDigitalTwinsDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="a186d-154">`Location <String>`: 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-154">`Location <String>`: The resource location.</span></span>
  - <span data-ttu-id="a186d-155">`[Tag <IDigitalTwinsResourceTags>]`: 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-155">`[Tag <IDigitalTwinsResourceTags>]`: The resource tags.</span></span>
    - <span data-ttu-id="a186d-156">`[(Any) <String>]`: 이 개체에 속성을 추가할 수 있는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a186d-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="a186d-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a186d-157">RELATED LINKS</span></span>

