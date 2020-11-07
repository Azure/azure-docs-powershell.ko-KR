---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 9d59a974a29743004228efb414a92627782bd8e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703805"
---
# <span data-ttu-id="7d639-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7d639-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="7d639-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d639-102">SYNOPSIS</span></span>
<span data-ttu-id="7d639-103">정책 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d639-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d639-104">SYNTAX</span></span>

### <span data-ttu-id="7d639-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7d639-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d639-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d639-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d639-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d639-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d639-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d639-108">IdParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d639-109">설명은</span><span class="sxs-lookup"><span data-stu-id="7d639-109">DESCRIPTION</span></span>
<span data-ttu-id="7d639-110">**제거-AzureRmPolicyDefinition** cmdlet은 정책 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-110">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="7d639-111">예제의</span><span class="sxs-lookup"><span data-stu-id="7d639-111">EXAMPLES</span></span>

### <span data-ttu-id="7d639-112">예제 1: 이름으로 정책 정의 제거</span><span class="sxs-lookup"><span data-stu-id="7d639-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="7d639-113">이 명령은 지정 된 정책 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="7d639-114">예제 2: 리소스 ID 별 정책 정의 제거</span><span class="sxs-lookup"><span data-stu-id="7d639-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="7d639-115">첫 번째 명령은 Get-AzureRmPolicyDefinition cmdlet을 사용 하 여 VMPolicyDefinition 이라는 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="7d639-116">명령이 $PolicyDefinition 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="7d639-117">두 번째 명령은 $PolicyDefinition의 **ResourceId** 속성으로 식별 되는 정책 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="7d639-118">변수</span><span class="sxs-lookup"><span data-stu-id="7d639-118">PARAMETERS</span></span>

### <span data-ttu-id="7d639-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7d639-119">-ApiVersion</span></span>
<span data-ttu-id="7d639-120">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7d639-121">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7d639-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d639-122">-DefaultProfile</span></span>
<span data-ttu-id="7d639-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7d639-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d639-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7d639-124">-Force</span></span>
<span data-ttu-id="7d639-125">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7d639-126">-Id</span><span class="sxs-lookup"><span data-stu-id="7d639-126">-Id</span></span>
<span data-ttu-id="7d639-127">이 cmdlet이 제거 하는 정책 정의에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7d639-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7d639-128">-InformationAction</span></span>
<span data-ttu-id="7d639-129">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="7d639-130">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7d639-131">하기로</span><span class="sxs-lookup"><span data-stu-id="7d639-131">Continue</span></span>
- <span data-ttu-id="7d639-132">숨기기</span><span class="sxs-lookup"><span data-stu-id="7d639-132">Ignore</span></span>
- <span data-ttu-id="7d639-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="7d639-133">Inquire</span></span>
- <span data-ttu-id="7d639-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7d639-134">SilentlyContinue</span></span>
- <span data-ttu-id="7d639-135">중지가</span><span class="sxs-lookup"><span data-stu-id="7d639-135">Stop</span></span>
- <span data-ttu-id="7d639-136">대기</span><span class="sxs-lookup"><span data-stu-id="7d639-136">Suspend</span></span>

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

### <span data-ttu-id="7d639-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7d639-137">-InformationVariable</span></span>
<span data-ttu-id="7d639-138">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7d639-139">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="7d639-139">-ManagementGroupName</span></span>
<span data-ttu-id="7d639-140">삭제할 정책 정의의 관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-140">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="7d639-141">-이름</span><span class="sxs-lookup"><span data-stu-id="7d639-141">-Name</span></span>
<span data-ttu-id="7d639-142">이 cmdlet이 제거 하는 정책 정의의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-142">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d639-143">-Pre</span><span class="sxs-lookup"><span data-stu-id="7d639-143">-Pre</span></span>
<span data-ttu-id="7d639-144">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7d639-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d639-145">-SubscriptionId</span></span>
<span data-ttu-id="7d639-146">삭제할 정책 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-146">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="7d639-147">-확인</span><span class="sxs-lookup"><span data-stu-id="7d639-147">-Confirm</span></span>
<span data-ttu-id="7d639-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d639-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d639-149">-WhatIf</span></span>
<span data-ttu-id="7d639-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d639-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d639-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d639-152">CommonParameters</span></span>
<span data-ttu-id="7d639-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d639-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d639-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d639-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d639-155">입력</span><span class="sxs-lookup"><span data-stu-id="7d639-155">INPUTS</span></span>

## <span data-ttu-id="7d639-156">출력</span><span class="sxs-lookup"><span data-stu-id="7d639-156">OUTPUTS</span></span>

## <span data-ttu-id="7d639-157">상속자</span><span class="sxs-lookup"><span data-stu-id="7d639-157">NOTES</span></span>

## <span data-ttu-id="7d639-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d639-158">RELATED LINKS</span></span>

[<span data-ttu-id="7d639-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7d639-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="7d639-160">새로운 AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7d639-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="7d639-161">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7d639-161">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


