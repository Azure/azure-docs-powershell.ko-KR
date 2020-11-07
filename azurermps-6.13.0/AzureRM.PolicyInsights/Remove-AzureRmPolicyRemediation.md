---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/remove-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Remove-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Remove-AzureRmPolicyRemediation.md
ms.openlocfilehash: ec5becd714b034789aeeb8449a63012232c99d5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702301"
---
# <span data-ttu-id="926d0-101">Remove-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="926d0-101">Remove-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="926d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="926d0-102">SYNOPSIS</span></span>
<span data-ttu-id="926d0-103">정책 업데이트를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-103">Deletes a policy remediation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="926d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="926d0-104">SYNTAX</span></span>

### <span data-ttu-id="926d0-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="926d0-105">ByName (Default)</span></span>
```
Remove-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="926d0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="926d0-106">ByResourceId</span></span>
```
Remove-AzureRmPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="926d0-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="926d0-107">ByInputObject</span></span>
```
Remove-AzureRmPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="926d0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="926d0-108">DESCRIPTION</span></span>
<span data-ttu-id="926d0-109">**AzureRmPolicyRemediation** cmdlet은 정책 수정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-109">The **Remove-AzureRmPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="926d0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="926d0-110">EXAMPLES</span></span>

### <span data-ttu-id="926d0-111">예제 1: 리소스 그룹 범위에서 정책 업데이트 삭제</span><span class="sxs-lookup"><span data-stu-id="926d0-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="926d0-112">이 명령은 리소스 그룹 ' myRG '에서 ' remediation1 ' 인 재구성을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="926d0-113">예제 2: 파이핑을 통해 관리 그룹 재구성 삭제</span><span class="sxs-lookup"><span data-stu-id="926d0-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzureRmPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzureRmPolicyRemediation -Confirm
```

<span data-ttu-id="926d0-114">이 명령은 관리 그룹 ' mg1 '에서 ' remediation1 ' 인 재구성을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="926d0-115">리소스를 삭제 하기 전에 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="926d0-116">예제 3: 정책 업데이트 취소 및 삭제</span><span class="sxs-lookup"><span data-stu-id="926d0-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="926d0-117">이 명령은 리소스 그룹 ' myRG '에서 ' remediation1 ' 인 재구성을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="926d0-118">재구성이 진행 중인 경우 삭제 하기 전에 취소 됩니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="926d0-119">변수</span><span class="sxs-lookup"><span data-stu-id="926d0-119">PARAMETERS</span></span>

### <span data-ttu-id="926d0-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="926d0-120">-AllowStop</span></span>
<span data-ttu-id="926d0-121">진행 중인 재구성을 취소 하도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="926d0-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="926d0-122">-AsJob</span></span>
<span data-ttu-id="926d0-123">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="926d0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="926d0-124">-DefaultProfile</span></span>
<span data-ttu-id="926d0-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="926d0-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="926d0-126">-InputObject</span></span>
<span data-ttu-id="926d0-127">업데이트 관리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-127">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="926d0-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="926d0-128">-ManagementGroupName</span></span>
<span data-ttu-id="926d0-129">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-129">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="926d0-130">-이름</span><span class="sxs-lookup"><span data-stu-id="926d0-130">-Name</span></span>
<span data-ttu-id="926d0-131">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-131">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="926d0-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="926d0-132">-PassThru</span></span>
<span data-ttu-id="926d0-133">명령이 성공적으로 완료 되 면 True를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="926d0-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="926d0-134">-ResourceGroupName</span></span>
<span data-ttu-id="926d0-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="926d0-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="926d0-136">-ResourceId</span></span>
<span data-ttu-id="926d0-137">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-137">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="926d0-138">-범위</span><span class="sxs-lookup"><span data-stu-id="926d0-138">-Scope</span></span>
<span data-ttu-id="926d0-139">리소스의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-139">Scope of the resource.</span></span>
<span data-ttu-id="926d0-140">즉.</span><span class="sxs-lookup"><span data-stu-id="926d0-140">E.g.</span></span>
<span data-ttu-id="926d0-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="926d0-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="926d0-142">-확인</span><span class="sxs-lookup"><span data-stu-id="926d0-142">-Confirm</span></span>
<span data-ttu-id="926d0-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="926d0-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="926d0-144">-WhatIf</span></span>
<span data-ttu-id="926d0-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="926d0-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="926d0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="926d0-147">CommonParameters</span></span>
<span data-ttu-id="926d0-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="926d0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="926d0-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="926d0-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="926d0-150">입력</span><span class="sxs-lookup"><span data-stu-id="926d0-150">INPUTS</span></span>

### <span data-ttu-id="926d0-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="926d0-151">System.String</span></span>

### <span data-ttu-id="926d0-152">Microsoft. Azure. m. m. m. 업데이트. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="926d0-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="926d0-153">출력</span><span class="sxs-lookup"><span data-stu-id="926d0-153">OUTPUTS</span></span>

### <span data-ttu-id="926d0-154">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="926d0-154">System.Boolean</span></span>

## <span data-ttu-id="926d0-155">상속자</span><span class="sxs-lookup"><span data-stu-id="926d0-155">NOTES</span></span>

## <span data-ttu-id="926d0-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="926d0-156">RELATED LINKS</span></span>
