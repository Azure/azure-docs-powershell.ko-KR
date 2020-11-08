---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 9f6f23babc1dfaf947a7eb8cea88011ff184cce7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041737"
---
# <span data-ttu-id="da9e5-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="da9e5-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="da9e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da9e5-102">SYNOPSIS</span></span>
<span data-ttu-id="da9e5-103">정책 정의를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="da9e5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="da9e5-104">SYNTAX</span></span>

### <span data-ttu-id="da9e5-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="da9e5-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da9e5-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="da9e5-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da9e5-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da9e5-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da9e5-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da9e5-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da9e5-109">설명은</span><span class="sxs-lookup"><span data-stu-id="da9e5-109">DESCRIPTION</span></span>
<span data-ttu-id="da9e5-110">**Set-AzPolicyDefinition** cmdlet은 정책 정의를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="da9e5-111">예제의</span><span class="sxs-lookup"><span data-stu-id="da9e5-111">EXAMPLES</span></span>

### <span data-ttu-id="da9e5-112">예제 1: 정책 정의에 대 한 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="da9e5-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="da9e5-113">첫 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용 하 여 VMPolicyDefinition 이라는 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="da9e5-114">명령이 $PolicyDefinition 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="da9e5-115">두 번째 명령은 $PolicyDefinition의 **ResourceId** 속성으로 식별 되는 정책 정의에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="da9e5-116">예제 2: 정책 정의 모드 업데이트</span><span class="sxs-lookup"><span data-stu-id="da9e5-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="da9e5-117">이 명령은 Set-AzPolicyDefinition cmdlet을 사용 하 여 VMPolicyDefinition 이라는 정책 정의를 업데이트 하 여 mode 속성을 ' 모두 '로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="da9e5-118">예제 3: 정책 정의의 메타 데이터 업데이트</span><span class="sxs-lookup"><span data-stu-id="da9e5-118">Example 3: Update the metadata of a policy definition</span></span>
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

<span data-ttu-id="da9e5-119">이 명령은 "가상 컴퓨터" 범주를 나타내기 위해 VMPolicyDefinition 이라는 정책 정의의 메타 데이터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-119">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="da9e5-120">변수</span><span class="sxs-lookup"><span data-stu-id="da9e5-120">PARAMETERS</span></span>

### <span data-ttu-id="da9e5-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="da9e5-121">-ApiVersion</span></span>
<span data-ttu-id="da9e5-122">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="da9e5-123">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="da9e5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da9e5-124">-DefaultProfile</span></span>
<span data-ttu-id="da9e5-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="da9e5-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da9e5-126">-설명</span><span class="sxs-lookup"><span data-stu-id="da9e5-126">-Description</span></span>
<span data-ttu-id="da9e5-127">정책 정의에 대 한 새 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-127">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="da9e5-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="da9e5-128">-DisplayName</span></span>
<span data-ttu-id="da9e5-129">정책 정의에 대 한 새 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-129">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="da9e5-130">-Id</span><span class="sxs-lookup"><span data-stu-id="da9e5-130">-Id</span></span>
<span data-ttu-id="da9e5-131">이 cmdlet이 수정 하는 정책 정의에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-131">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="da9e5-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="da9e5-132">-ManagementGroupName</span></span>
<span data-ttu-id="da9e5-133">업데이트할 정책 정의의 관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-133">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="da9e5-134">-Metadata</span><span class="sxs-lookup"><span data-stu-id="da9e5-134">-Metadata</span></span>
<span data-ttu-id="da9e5-135">정책 정의에 대 한 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-135">The metadata for policy definition.</span></span> <span data-ttu-id="da9e5-136">메타 데이터를 포함 하는 파일 이름에 대 한 경로 이거나 메타 데이터 인 string 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-136">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="da9e5-137">-모드</span><span class="sxs-lookup"><span data-stu-id="da9e5-137">-Mode</span></span>
<span data-ttu-id="da9e5-138">새 정책 정의의 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-138">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="da9e5-139">-이름</span><span class="sxs-lookup"><span data-stu-id="da9e5-139">-Name</span></span>
<span data-ttu-id="da9e5-140">이 cmdlet이 수정 하는 정책 정의의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-140">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="da9e5-141">-Parameter</span><span class="sxs-lookup"><span data-stu-id="da9e5-141">-Parameter</span></span>
<span data-ttu-id="da9e5-142">정책 정의에 대 한 매개 변수 선언입니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-142">The parameters declaration for policy definition.</span></span> <span data-ttu-id="da9e5-143">매개 변수 선언을 포함 하는 uri 또는 파일 이름 또는 매개 변수 선언 문자열의 경로일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-143">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="da9e5-144">-정책</span><span class="sxs-lookup"><span data-stu-id="da9e5-144">-Policy</span></span>
<span data-ttu-id="da9e5-145">정책 정의에 대 한 새 정책 규칙을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-145">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="da9e5-146">Json 파일의 경로 또는 JSON (JavaScript Object Notation) 형식의 정책을 포함 하는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-146">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="da9e5-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="da9e5-147">-Pre</span></span>
<span data-ttu-id="da9e5-148">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="da9e5-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da9e5-149">-SubscriptionId</span></span>
<span data-ttu-id="da9e5-150">업데이트할 정책 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-150">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="da9e5-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da9e5-151">CommonParameters</span></span>
<span data-ttu-id="da9e5-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da9e5-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da9e5-153">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da9e5-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da9e5-154">입력</span><span class="sxs-lookup"><span data-stu-id="da9e5-154">INPUTS</span></span>

### <span data-ttu-id="da9e5-155">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="da9e5-155">System.String</span></span>

### <span data-ttu-id="da9e5-156">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="da9e5-156">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="da9e5-157">출력</span><span class="sxs-lookup"><span data-stu-id="da9e5-157">OUTPUTS</span></span>

### <span data-ttu-id="da9e5-158">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="da9e5-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="da9e5-159">상속자</span><span class="sxs-lookup"><span data-stu-id="da9e5-159">NOTES</span></span>

## <span data-ttu-id="da9e5-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da9e5-160">RELATED LINKS</span></span>

[<span data-ttu-id="da9e5-161">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="da9e5-161">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="da9e5-162">새로운 AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="da9e5-162">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="da9e5-163">제거-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="da9e5-163">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


