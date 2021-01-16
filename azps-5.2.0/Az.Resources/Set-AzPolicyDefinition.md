---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 3aed403965bc48a26044b930fdf5cc9e9a93bbbe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351729"
---
# <span data-ttu-id="f069c-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f069c-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="f069c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f069c-102">SYNOPSIS</span></span>
<span data-ttu-id="f069c-103">정책 정의를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="f069c-104">구문</span><span class="sxs-lookup"><span data-stu-id="f069c-104">SYNTAX</span></span>

### <span data-ttu-id="f069c-105">NameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f069c-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f069c-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f069c-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f069c-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f069c-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f069c-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f069c-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f069c-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f069c-109">InputObjectParameterSet</span></span>
```
Set-AzPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>] [-Metadata <String>]
 [-Parameter <String>] [-Mode <String>] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f069c-110">설명</span><span class="sxs-lookup"><span data-stu-id="f069c-110">DESCRIPTION</span></span>
<span data-ttu-id="f069c-111">**Set-AzPolicyDefinition** cmdlet은 정책 정의를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-111">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="f069c-112">예제</span><span class="sxs-lookup"><span data-stu-id="f069c-112">EXAMPLES</span></span>

### <span data-ttu-id="f069c-113">예제 1: 정책 정의에 대한 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="f069c-113">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="f069c-114">첫 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용하여 VMPolicyDefinition이라는 정책 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="f069c-115">이 명령은 해당 개체를 $PolicyDefinition 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-115">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="f069c-116">두 번째 명령은 리소스의 **ResourceId** 속성으로 식별되는 정책 정의에 대한 설명을 $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="f069c-116">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="f069c-117">예제 2: 정책 정의의 모드 업데이트</span><span class="sxs-lookup"><span data-stu-id="f069c-117">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="f069c-118">이 명령은 Set-AzPolicyDefinition cmdlet을 사용하여 해당 모드 속성을 '모두'로 설정하여 VMPolicyDefinition이라는 정책 정의를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-118">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="f069c-119">예제 3: 정책 정의의 메타데이터 업데이트</span><span class="sxs-lookup"><span data-stu-id="f069c-119">Example 3: Update the metadata of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="f069c-120">이 명령은 해당 범주가 "Virtual Machine"이라는 것을 나타내기 위해 VMPolicyDefinition이라는 정책 정의의 메타데이터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-120">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="f069c-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f069c-121">PARAMETERS</span></span>

### <span data-ttu-id="f069c-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f069c-122">-ApiVersion</span></span>
<span data-ttu-id="f069c-123">사용할 리소스 공급자 API의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f069c-124">버전을 지정하지 않으면 이 cmdlet은 사용 가능한 최신 버전을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f069c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f069c-125">-DefaultProfile</span></span>
<span data-ttu-id="f069c-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f069c-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f069c-127">-Description</span><span class="sxs-lookup"><span data-stu-id="f069c-127">-Description</span></span>
<span data-ttu-id="f069c-128">정책 정의에 대한 새 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-128">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="f069c-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f069c-129">-DisplayName</span></span>
<span data-ttu-id="f069c-130">정책 정의에 대한 새 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-130">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="f069c-131">-Id</span><span class="sxs-lookup"><span data-stu-id="f069c-131">-Id</span></span>
<span data-ttu-id="f069c-132">이 cmdlet이 수정하는 정책 정의에 대한 정식 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-132">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f069c-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f069c-133">-InputObject</span></span>
<span data-ttu-id="f069c-134">다른 cmdlet에서 출력된 업데이트할 정책 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-134">The policy definition object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f069c-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f069c-135">-ManagementGroupName</span></span>
<span data-ttu-id="f069c-136">업데이트할 정책 정의의 관리 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-136">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="f069c-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f069c-137">-Metadata</span></span>
<span data-ttu-id="f069c-138">정책 정의에 대한 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-138">The metadata for policy definition.</span></span> <span data-ttu-id="f069c-139">메타데이터를 포함하는 파일 이름의 경로 또는 메타데이터를 문자열로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-139">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="f069c-140">-Mode</span><span class="sxs-lookup"><span data-stu-id="f069c-140">-Mode</span></span>
<span data-ttu-id="f069c-141">새 정책 정의의 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-141">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="f069c-142">-Name</span><span class="sxs-lookup"><span data-stu-id="f069c-142">-Name</span></span>
<span data-ttu-id="f069c-143">이 cmdlet이 수정하는 정책 정의의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-143">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f069c-144">-Parameter</span><span class="sxs-lookup"><span data-stu-id="f069c-144">-Parameter</span></span>
<span data-ttu-id="f069c-145">정책 정의에 대한 매개 변수 선언입니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="f069c-146">파일 이름에 대한 경로 또는 매개 변수 선언을 포함하는 URI 또는 매개 변수 선언을 문자열로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-146">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="f069c-147">-Policy</span><span class="sxs-lookup"><span data-stu-id="f069c-147">-Policy</span></span>
<span data-ttu-id="f069c-148">정책 정의에 대한 새 정책 규칙을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-148">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="f069c-149">.json 파일의 경로 또는 JSON(JavaScript Object Notation) 형식으로 정책을 포함하는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-149">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="f069c-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="f069c-150">-Pre</span></span>
<span data-ttu-id="f069c-151">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f069c-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f069c-152">-SubscriptionId</span></span>
<span data-ttu-id="f069c-153">업데이트할 정책 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-153">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="f069c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f069c-154">CommonParameters</span></span>
<span data-ttu-id="f069c-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f069c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f069c-156">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f069c-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f069c-157">입력</span><span class="sxs-lookup"><span data-stu-id="f069c-157">INPUTS</span></span>

### <span data-ttu-id="f069c-158">System.String</span><span class="sxs-lookup"><span data-stu-id="f069c-158">System.String</span></span>

### <span data-ttu-id="f069c-159">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f069c-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f069c-160">출력</span><span class="sxs-lookup"><span data-stu-id="f069c-160">OUTPUTS</span></span>

### <span data-ttu-id="f069c-161">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="f069c-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f069c-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f069c-162">NOTES</span></span>

## <span data-ttu-id="f069c-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f069c-163">RELATED LINKS</span></span>

[<span data-ttu-id="f069c-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f069c-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="f069c-165">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f069c-165">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="f069c-166">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f069c-166">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


