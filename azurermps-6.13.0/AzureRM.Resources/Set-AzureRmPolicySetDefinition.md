---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: d558e7104027e4c3fcef3b6e8d8427d5fd3802fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711016"
---
# <span data-ttu-id="94039-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="94039-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="94039-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94039-102">SYNOPSIS</span></span>
<span data-ttu-id="94039-103">정책 집합 정의를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94039-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94039-104">구문과</span><span class="sxs-lookup"><span data-stu-id="94039-104">SYNTAX</span></span>

### <span data-ttu-id="94039-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="94039-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94039-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="94039-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94039-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94039-107">SubscriptionIdParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94039-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94039-108">IdParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94039-109">설명은</span><span class="sxs-lookup"><span data-stu-id="94039-109">DESCRIPTION</span></span>
<span data-ttu-id="94039-110">**Set-AzureRmPolicySetDefinition** cmdlet은 정책 정의를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94039-110">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="94039-111">예제의</span><span class="sxs-lookup"><span data-stu-id="94039-111">EXAMPLES</span></span>

### <span data-ttu-id="94039-112">예제 1: 정책 집합 정의에 대 한 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="94039-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="94039-113">첫 번째 명령은 Get-AzureRmPolicySetDefinition cmdlet을 사용 하 여 정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94039-113">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="94039-114">명령이 $PolicySetDefinition 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="94039-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="94039-115">두 번째 명령은 $PolicySetDefinition의 **ResourceId** 속성으로 식별 되는 정책 집합 정의에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="94039-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="94039-116">변수</span><span class="sxs-lookup"><span data-stu-id="94039-116">PARAMETERS</span></span>

### <span data-ttu-id="94039-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="94039-117">-ApiVersion</span></span>
<span data-ttu-id="94039-118">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="94039-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="94039-119">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="94039-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="94039-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94039-120">-DefaultProfile</span></span>
<span data-ttu-id="94039-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="94039-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94039-122">-설명</span><span class="sxs-lookup"><span data-stu-id="94039-122">-Description</span></span>
<span data-ttu-id="94039-123">정책 집합 정의에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="94039-123">The description for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94039-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="94039-124">-DisplayName</span></span>
<span data-ttu-id="94039-125">정책 집합 정의의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94039-125">The display name for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94039-126">-Id</span><span class="sxs-lookup"><span data-stu-id="94039-126">-Id</span></span>
<span data-ttu-id="94039-127">구독을 포함 하는 정규화 된 정책 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="94039-127">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="94039-128">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="94039-128">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94039-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="94039-129">-ManagementGroupName</span></span>
<span data-ttu-id="94039-130">업데이트할 정책 집합 정의의 관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94039-130">The name of the management group of the policy set definition to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94039-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="94039-131">-Metadata</span></span>
<span data-ttu-id="94039-132">업데이트 된 정책 집합 정의의 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="94039-132">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="94039-133">메타 데이터를 포함 하는 파일 이름의 경로 이거나 메타 데이터를 문자열로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94039-133">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94039-134">-이름</span><span class="sxs-lookup"><span data-stu-id="94039-134">-Name</span></span>
<span data-ttu-id="94039-135">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94039-135">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94039-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="94039-136">-Parameter</span></span>
<span data-ttu-id="94039-137">업데이트 된 정책 집합 정의의 매개 변수 선언입니다.</span><span class="sxs-lookup"><span data-stu-id="94039-137">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="94039-138">매개 변수 선언을 포함 하는 uri 또는 파일 이름에 대 한 경로 이거나 매개 변수 선언이 string 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94039-138">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94039-139">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="94039-139">-PolicyDefinition</span></span>
<span data-ttu-id="94039-140">정책 집합 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="94039-140">The policy set definition.</span></span> <span data-ttu-id="94039-141">이는 정책 정의를 포함 하는 파일 이름에 대 한 경로 이거나 정책 집합 정의를 문자열로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94039-141">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94039-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="94039-142">-Pre</span></span>
<span data-ttu-id="94039-143">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="94039-143">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="94039-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94039-144">-SubscriptionId</span></span>
<span data-ttu-id="94039-145">업데이트할 정책 집합 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="94039-145">The subscription ID of the policy set definition to update.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94039-146">-확인</span><span class="sxs-lookup"><span data-stu-id="94039-146">-Confirm</span></span>
<span data-ttu-id="94039-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="94039-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94039-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94039-148">-WhatIf</span></span>
<span data-ttu-id="94039-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="94039-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94039-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94039-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94039-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94039-151">CommonParameters</span></span>
<span data-ttu-id="94039-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="94039-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94039-153">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94039-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94039-154">입력</span><span class="sxs-lookup"><span data-stu-id="94039-154">INPUTS</span></span>

### <span data-ttu-id="94039-155">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="94039-155">System.String</span></span>

### <span data-ttu-id="94039-156">시스템 Null 허용 ' 1 [[b77a5c561934e089], mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="94039-156">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="94039-157">출력</span><span class="sxs-lookup"><span data-stu-id="94039-157">OUTPUTS</span></span>

### <span data-ttu-id="94039-158">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="94039-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="94039-159">상속자</span><span class="sxs-lookup"><span data-stu-id="94039-159">NOTES</span></span>

## <span data-ttu-id="94039-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94039-160">RELATED LINKS</span></span>
