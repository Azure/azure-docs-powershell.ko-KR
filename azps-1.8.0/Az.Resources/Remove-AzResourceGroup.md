---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
ms.openlocfilehash: 7878932b0e7a2aad6e171c39e546ad86b2ea0a7c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699335"
---
# <span data-ttu-id="4211a-101">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4211a-101">Remove-AzResourceGroup</span></span>

## <span data-ttu-id="4211a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4211a-102">SYNOPSIS</span></span>
<span data-ttu-id="4211a-103">리소스 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-103">Removes a resource group.</span></span>

## <span data-ttu-id="4211a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4211a-104">SYNTAX</span></span>

### <span data-ttu-id="4211a-105">RemoveByResourceGroupName (기본값)</span><span class="sxs-lookup"><span data-stu-id="4211a-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4211a-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="4211a-106">RemoveByResourceGroupId</span></span>
```
Remove-AzResourceGroup -Id <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4211a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4211a-107">DESCRIPTION</span></span>
<span data-ttu-id="4211a-108">**AzResourceGroup** cmdlet은 현재 구독에서 Azure 리소스 그룹과 해당 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-108">The **Remove-AzResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="4211a-109">리소스를 삭제 하 되 리소스 그룹을 유지 하려면 Remove-AzResource cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-109">To delete a resource, but leave the resource group, use the Remove-AzResource cmdlet.</span></span>

## <span data-ttu-id="4211a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4211a-110">EXAMPLES</span></span>

### <span data-ttu-id="4211a-111">예제 1: 리소스 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="4211a-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="4211a-112">이 명령은 구독에서 ContosoRG01 리소스 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="4211a-113">Cmdlet에서 확인을 요청 하 고 출력을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="4211a-114">예제 2: 확인 하지 않고 리소스 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="4211a-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzResourceGroup -Name "ContosoRG01" | Remove-AzResourceGroup -Verbose -Force
```

<span data-ttu-id="4211a-115">이 명령은 Get-AzResourceGroup cmdlet을 사용 하 여 리소스 그룹 ContosoRG01을 얻은 다음 pipeline 연산자를 사용 하 여 **Remove-AzResourceGroup** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-115">This command uses the Get-AzResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="4211a-116">*Verbose* 공용 매개 변수는 연산에 대 한 상태 정보를 가져오며 *Force* 매개 변수는 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-116">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="4211a-117">예제 3: 모든 리소스 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="4211a-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Remove-AzResourceGroup
```

<span data-ttu-id="4211a-118">이 명령은 **AzResourceGroup** cmdlet을 사용 하 여 모든 리소스 그룹을 가져와 해당 파이프라인 연산자를 사용 하 여 **Remove-AzResourceGroup** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-118">This command uses the **Get-AzResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="4211a-119">변수</span><span class="sxs-lookup"><span data-stu-id="4211a-119">PARAMETERS</span></span>

### <span data-ttu-id="4211a-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4211a-120">-ApiVersion</span></span>
<span data-ttu-id="4211a-121">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="4211a-122">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="4211a-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4211a-123">-AsJob</span></span>
<span data-ttu-id="4211a-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4211a-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4211a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4211a-125">-DefaultProfile</span></span>
<span data-ttu-id="4211a-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4211a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4211a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="4211a-127">-Force</span></span>
<span data-ttu-id="4211a-128">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4211a-129">-Id</span><span class="sxs-lookup"><span data-stu-id="4211a-129">-Id</span></span>
<span data-ttu-id="4211a-130">제거할 리소스 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="4211a-131">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4211a-132">-이름</span><span class="sxs-lookup"><span data-stu-id="4211a-132">-Name</span></span>
<span data-ttu-id="4211a-133">제거할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="4211a-134">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-134">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4211a-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="4211a-135">-Pre</span></span>
<span data-ttu-id="4211a-136">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4211a-137">-확인</span><span class="sxs-lookup"><span data-stu-id="4211a-137">-Confirm</span></span>
<span data-ttu-id="4211a-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4211a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4211a-139">-WhatIf</span></span>
<span data-ttu-id="4211a-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4211a-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4211a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4211a-142">CommonParameters</span></span>
<span data-ttu-id="4211a-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4211a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4211a-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4211a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4211a-145">입력</span><span class="sxs-lookup"><span data-stu-id="4211a-145">INPUTS</span></span>

### <span data-ttu-id="4211a-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4211a-146">System.String</span></span>

## <span data-ttu-id="4211a-147">출력</span><span class="sxs-lookup"><span data-stu-id="4211a-147">OUTPUTS</span></span>

### <span data-ttu-id="4211a-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="4211a-148">System.Boolean</span></span>

## <span data-ttu-id="4211a-149">상속자</span><span class="sxs-lookup"><span data-stu-id="4211a-149">NOTES</span></span>

## <span data-ttu-id="4211a-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4211a-150">RELATED LINKS</span></span>

[<span data-ttu-id="4211a-151">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4211a-151">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="4211a-152">새로운 AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4211a-152">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="4211a-153">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4211a-153">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)

