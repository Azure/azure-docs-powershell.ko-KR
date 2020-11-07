---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: 5b6d514fc41c909fdd48b6a13ba85ab5836a5668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873269"
---
# <span data-ttu-id="85c65-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="85c65-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="85c65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85c65-102">SYNOPSIS</span></span>
<span data-ttu-id="85c65-103">정책 집합 정의를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="85c65-104">구문과</span><span class="sxs-lookup"><span data-stu-id="85c65-104">SYNTAX</span></span>

### <span data-ttu-id="85c65-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="85c65-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85c65-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="85c65-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85c65-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85c65-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85c65-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85c65-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85c65-109">설명은</span><span class="sxs-lookup"><span data-stu-id="85c65-109">DESCRIPTION</span></span>
<span data-ttu-id="85c65-110">**Set-AzPolicySetDefinition** cmdlet은 정책 정의를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="85c65-111">예제의</span><span class="sxs-lookup"><span data-stu-id="85c65-111">EXAMPLES</span></span>

### <span data-ttu-id="85c65-112">예제 1: 정책 집합 정의에 대 한 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="85c65-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="85c65-113">첫 번째 명령은 Get-AzPolicySetDefinition cmdlet을 사용 하 여 정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="85c65-114">명령이 $PolicySetDefinition 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="85c65-115">두 번째 명령은 $PolicySetDefinition의 **ResourceId** 속성으로 식별 되는 정책 집합 정의에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="85c65-116">예제 2: 정책 집합 정의의 메타 데이터 업데이트</span><span class="sxs-lookup"><span data-stu-id="85c65-116">Example 2: Update the metadata of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}'


Name                  : VMPolicySetDefinition
ResourceId            : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
ResourceName          : VMPolicySetDefinition
ResourceType          : Microsoft.Authorization/policySetDefinitions
SubscriptionId        : 11111111-1111-1111-1111-111111111111
Properties            : @{displayName=VMPolicySetDefinition; policyType=Custom; metadata=; parameters=; policyDefinitions=System.Object[]}
PolicySetDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
```

<span data-ttu-id="85c65-117">이 명령은 ' 가상 머신 ' 범주를 나타내기 위해 VMPolicySetDefinition 이라는 정책 집합 정의의 메타 데이터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-117">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="85c65-118">변수</span><span class="sxs-lookup"><span data-stu-id="85c65-118">PARAMETERS</span></span>

### <span data-ttu-id="85c65-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="85c65-119">-ApiVersion</span></span>
<span data-ttu-id="85c65-120">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="85c65-121">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="85c65-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c65-122">-DefaultProfile</span></span>
<span data-ttu-id="85c65-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="85c65-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85c65-124">-설명</span><span class="sxs-lookup"><span data-stu-id="85c65-124">-Description</span></span>
<span data-ttu-id="85c65-125">정책 집합 정의에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-125">The description for policy set definition.</span></span>

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

### <span data-ttu-id="85c65-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="85c65-126">-DisplayName</span></span>
<span data-ttu-id="85c65-127">정책 집합 정의의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-127">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="85c65-128">-Id</span><span class="sxs-lookup"><span data-stu-id="85c65-128">-Id</span></span>
<span data-ttu-id="85c65-129">구독을 포함 하는 정규화 된 정책 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-129">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="85c65-130">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="85c65-130">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="85c65-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="85c65-131">-ManagementGroupName</span></span>
<span data-ttu-id="85c65-132">업데이트할 정책 집합 정의의 관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-132">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="85c65-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="85c65-133">-Metadata</span></span>
<span data-ttu-id="85c65-134">업데이트 된 정책 집합 정의의 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-134">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="85c65-135">메타 데이터를 포함 하는 파일 이름의 경로 이거나 메타 데이터를 문자열로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-135">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="85c65-136">-이름</span><span class="sxs-lookup"><span data-stu-id="85c65-136">-Name</span></span>
<span data-ttu-id="85c65-137">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-137">The policy set definition name.</span></span>

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

### <span data-ttu-id="85c65-138">-Parameter</span><span class="sxs-lookup"><span data-stu-id="85c65-138">-Parameter</span></span>
<span data-ttu-id="85c65-139">업데이트 된 정책 집합 정의의 매개 변수 선언입니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-139">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="85c65-140">매개 변수 선언을 포함 하는 uri 또는 파일 이름에 대 한 경로 이거나 매개 변수 선언이 string 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-140">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

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

### <span data-ttu-id="85c65-141">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="85c65-141">-PolicyDefinition</span></span>
<span data-ttu-id="85c65-142">정책 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-142">The policy definitions.</span></span> <span data-ttu-id="85c65-143">이는 정책 정의를 포함 하는 파일 이름에 대 한 경로 이거나 문자열 형식으로 된 정책 정의 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-143">This can either be a path to a file name containing the policy definitions, or the policy definitions as string.</span></span>

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

### <span data-ttu-id="85c65-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="85c65-144">-Pre</span></span>
<span data-ttu-id="85c65-145">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="85c65-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85c65-146">-SubscriptionId</span></span>
<span data-ttu-id="85c65-147">업데이트할 정책 집합 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-147">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="85c65-148">-확인</span><span class="sxs-lookup"><span data-stu-id="85c65-148">-Confirm</span></span>
<span data-ttu-id="85c65-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85c65-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85c65-150">-WhatIf</span></span>
<span data-ttu-id="85c65-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85c65-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85c65-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c65-153">CommonParameters</span></span>
<span data-ttu-id="85c65-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="85c65-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c65-155">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="85c65-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c65-156">입력</span><span class="sxs-lookup"><span data-stu-id="85c65-156">INPUTS</span></span>

### <span data-ttu-id="85c65-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="85c65-157">System.String</span></span>

### <span data-ttu-id="85c65-158">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="85c65-158">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="85c65-159">출력</span><span class="sxs-lookup"><span data-stu-id="85c65-159">OUTPUTS</span></span>

### <span data-ttu-id="85c65-160">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="85c65-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="85c65-161">상속자</span><span class="sxs-lookup"><span data-stu-id="85c65-161">NOTES</span></span>

## <span data-ttu-id="85c65-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85c65-162">RELATED LINKS</span></span>
