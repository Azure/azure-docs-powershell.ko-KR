---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicydefinition
schema: 2.0.0
ms.openlocfilehash: aa6687efb331cbb702ea36c53cc02cd77cefd45d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880870"
---
# <span data-ttu-id="62c34-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="62c34-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="62c34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62c34-102">SYNOPSIS</span></span>
<span data-ttu-id="62c34-103">정책 정의를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62c34-104">구문과</span><span class="sxs-lookup"><span data-stu-id="62c34-104">SYNTAX</span></span>

### <span data-ttu-id="62c34-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="62c34-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="62c34-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="62c34-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="62c34-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62c34-107">SubscriptionIdParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="62c34-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62c34-108">IdParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="62c34-109">설명은</span><span class="sxs-lookup"><span data-stu-id="62c34-109">DESCRIPTION</span></span>
<span data-ttu-id="62c34-110">**Set-AzureRmPolicyDefinition** cmdlet은 정책 정의를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-110">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="62c34-111">예제의</span><span class="sxs-lookup"><span data-stu-id="62c34-111">EXAMPLES</span></span>

### <span data-ttu-id="62c34-112">예제 1: 정책 정의에 대 한 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="62c34-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="62c34-113">첫 번째 명령은 Get-AzureRmPolicyDefinition cmdlet을 사용 하 여 VMPolicyDefinition 이라는 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="62c34-114">명령이 $PolicyDefinition 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="62c34-115">두 번째 명령은 $PolicyDefinition의 **ResourceId** 속성으로 식별 되는 정책 정의에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="62c34-116">예제 2: 정책 정의 모드 업데이트</span><span class="sxs-lookup"><span data-stu-id="62c34-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="62c34-117">이 명령은 Set-AzureRmPolicyDefinition cmdlet을 사용 하 여 VMPolicyDefinition 이라는 정책 정의를 업데이트 하 여 mode 속성을 ' 모두 '로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzureRmPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="62c34-118">변수</span><span class="sxs-lookup"><span data-stu-id="62c34-118">PARAMETERS</span></span>

### <span data-ttu-id="62c34-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="62c34-119">-ApiVersion</span></span>
<span data-ttu-id="62c34-120">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="62c34-121">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="62c34-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c34-122">-DefaultProfile</span></span>
<span data-ttu-id="62c34-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="62c34-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62c34-124">-설명</span><span class="sxs-lookup"><span data-stu-id="62c34-124">-Description</span></span>
<span data-ttu-id="62c34-125">정책 정의에 대 한 새 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-125">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="62c34-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="62c34-126">-DisplayName</span></span>
<span data-ttu-id="62c34-127">정책 정의에 대 한 새 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-127">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="62c34-128">-Id</span><span class="sxs-lookup"><span data-stu-id="62c34-128">-Id</span></span>
<span data-ttu-id="62c34-129">이 cmdlet이 수정 하는 정책 정의에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="62c34-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="62c34-130">-InformationAction</span></span>
<span data-ttu-id="62c34-131">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-131">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="62c34-132">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="62c34-133">하기로</span><span class="sxs-lookup"><span data-stu-id="62c34-133">Continue</span></span>
- <span data-ttu-id="62c34-134">숨기기</span><span class="sxs-lookup"><span data-stu-id="62c34-134">Ignore</span></span>
- <span data-ttu-id="62c34-135">Inquire</span><span class="sxs-lookup"><span data-stu-id="62c34-135">Inquire</span></span>
- <span data-ttu-id="62c34-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="62c34-136">SilentlyContinue</span></span>
- <span data-ttu-id="62c34-137">중지가</span><span class="sxs-lookup"><span data-stu-id="62c34-137">Stop</span></span>
- <span data-ttu-id="62c34-138">대기</span><span class="sxs-lookup"><span data-stu-id="62c34-138">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c34-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="62c34-139">-InformationVariable</span></span>
<span data-ttu-id="62c34-140">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-140">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c34-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="62c34-141">-ManagementGroupName</span></span>
<span data-ttu-id="62c34-142">업데이트할 정책 정의의 관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-142">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="62c34-143">-Metadata</span><span class="sxs-lookup"><span data-stu-id="62c34-143">-Metadata</span></span>
<span data-ttu-id="62c34-144">정책 정의에 대 한 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-144">The metadata for policy definition.</span></span> <span data-ttu-id="62c34-145">메타 데이터를 포함 하는 파일 이름에 대 한 경로 이거나 메타 데이터 인 string 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-145">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="62c34-146">-모드</span><span class="sxs-lookup"><span data-stu-id="62c34-146">-Mode</span></span>
<span data-ttu-id="62c34-147">새 정책 정의의 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-147">The mode of the new policy definition.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62c34-148">-이름</span><span class="sxs-lookup"><span data-stu-id="62c34-148">-Name</span></span>
<span data-ttu-id="62c34-149">이 cmdlet이 수정 하는 정책 정의의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-149">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="62c34-150">-Parameter</span><span class="sxs-lookup"><span data-stu-id="62c34-150">-Parameter</span></span>
<span data-ttu-id="62c34-151">정책 정의에 대 한 매개 변수 선언입니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-151">The parameters declaration for policy definition.</span></span> <span data-ttu-id="62c34-152">매개 변수 선언을 포함 하는 uri 또는 파일 이름 또는 매개 변수 선언 문자열의 경로일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-152">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="62c34-153">-정책</span><span class="sxs-lookup"><span data-stu-id="62c34-153">-Policy</span></span>
<span data-ttu-id="62c34-154">정책 정의에 대 한 새 정책 규칙을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-154">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="62c34-155">Json 파일의 경로 또는 JSON (JavaScript Object Notation) 형식의 정책을 포함 하는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-155">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="62c34-156">-Pre</span><span class="sxs-lookup"><span data-stu-id="62c34-156">-Pre</span></span>
<span data-ttu-id="62c34-157">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-157">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="62c34-158">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62c34-158">-SubscriptionId</span></span>
<span data-ttu-id="62c34-159">업데이트할 정책 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-159">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="62c34-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c34-160">CommonParameters</span></span>
<span data-ttu-id="62c34-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62c34-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c34-162">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62c34-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c34-163">입력</span><span class="sxs-lookup"><span data-stu-id="62c34-163">INPUTS</span></span>

## <span data-ttu-id="62c34-164">출력</span><span class="sxs-lookup"><span data-stu-id="62c34-164">OUTPUTS</span></span>

## <span data-ttu-id="62c34-165">상속자</span><span class="sxs-lookup"><span data-stu-id="62c34-165">NOTES</span></span>

## <span data-ttu-id="62c34-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62c34-166">RELATED LINKS</span></span>

[<span data-ttu-id="62c34-167">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="62c34-167">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="62c34-168">새로운 AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="62c34-168">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="62c34-169">제거-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="62c34-169">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


