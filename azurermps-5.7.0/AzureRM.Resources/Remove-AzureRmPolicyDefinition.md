---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 68c4f94ea4fee91c03ab0c65cbcba0f025c3c43b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702142"
---
# <span data-ttu-id="994e1-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="994e1-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="994e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="994e1-102">SYNOPSIS</span></span>
<span data-ttu-id="994e1-103">정책 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="994e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="994e1-104">SYNTAX</span></span>

### <span data-ttu-id="994e1-105">RemoveByPolicyDefinitionName (기본값)</span><span class="sxs-lookup"><span data-stu-id="994e1-105">RemoveByPolicyDefinitionName (Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="994e1-106">RemoveByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="994e1-106">RemoveByPolicyDefinitionId</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="994e1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="994e1-107">DESCRIPTION</span></span>
<span data-ttu-id="994e1-108">**제거-AzureRmPolicyDefinition** cmdlet은 정책 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-108">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="994e1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="994e1-109">EXAMPLES</span></span>

### <span data-ttu-id="994e1-110">예제 1: 이름으로 정책 정의 제거</span><span class="sxs-lookup"><span data-stu-id="994e1-110">Example 1: Remove the policy definition by name</span></span>
```
PS C:\>Remove-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="994e1-111">이 명령은 지정 된 정책 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-111">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="994e1-112">예제 2: 리소스 ID 별 정책 정의 제거</span><span class="sxs-lookup"><span data-stu-id="994e1-112">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition" 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="994e1-113">첫 번째 명령은 Get-AzureRmPolicyDefinition cmdlet을 사용 하 여 VMPolicyDefinition 이라는 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="994e1-114">명령이 $PolicyDefinition 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-114">The command stores it in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="994e1-115">두 번째 명령은 $PolicyDefinition의 **ResourceId** 속성으로 식별 되는 정책 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-115">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="994e1-116">변수</span><span class="sxs-lookup"><span data-stu-id="994e1-116">PARAMETERS</span></span>

### <span data-ttu-id="994e1-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="994e1-117">-ApiVersion</span></span>
<span data-ttu-id="994e1-118">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="994e1-119">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994e1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="994e1-120">-DefaultProfile</span></span>
<span data-ttu-id="994e1-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="994e1-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994e1-122">-Force</span><span class="sxs-lookup"><span data-stu-id="994e1-122">-Force</span></span>
<span data-ttu-id="994e1-123">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994e1-124">-Id</span><span class="sxs-lookup"><span data-stu-id="994e1-124">-Id</span></span>
<span data-ttu-id="994e1-125">이 cmdlet이 제거 하는 정책 정의에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-125">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="994e1-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="994e1-126">-InformationAction</span></span>
<span data-ttu-id="994e1-127">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="994e1-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="994e1-129">하기로</span><span class="sxs-lookup"><span data-stu-id="994e1-129">Continue</span></span>
- <span data-ttu-id="994e1-130">숨기기</span><span class="sxs-lookup"><span data-stu-id="994e1-130">Ignore</span></span>
- <span data-ttu-id="994e1-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="994e1-131">Inquire</span></span>
- <span data-ttu-id="994e1-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="994e1-132">SilentlyContinue</span></span>
- <span data-ttu-id="994e1-133">중지가</span><span class="sxs-lookup"><span data-stu-id="994e1-133">Stop</span></span>
- <span data-ttu-id="994e1-134">대기</span><span class="sxs-lookup"><span data-stu-id="994e1-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994e1-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="994e1-135">-InformationVariable</span></span>
<span data-ttu-id="994e1-136">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994e1-137">-이름</span><span class="sxs-lookup"><span data-stu-id="994e1-137">-Name</span></span>
<span data-ttu-id="994e1-138">이 cmdlet이 제거 하는 정책 정의의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-138">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="994e1-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="994e1-139">-Pre</span></span>
<span data-ttu-id="994e1-140">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994e1-141">-확인</span><span class="sxs-lookup"><span data-stu-id="994e1-141">-Confirm</span></span>
<span data-ttu-id="994e1-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994e1-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="994e1-143">-WhatIf</span></span>
<span data-ttu-id="994e1-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="994e1-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994e1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="994e1-146">CommonParameters</span></span>
<span data-ttu-id="994e1-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="994e1-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="994e1-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="994e1-149">입력</span><span class="sxs-lookup"><span data-stu-id="994e1-149">INPUTS</span></span>

### <span data-ttu-id="994e1-150">않아야</span><span class="sxs-lookup"><span data-stu-id="994e1-150">None</span></span>
<span data-ttu-id="994e1-151">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="994e1-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="994e1-152">출력</span><span class="sxs-lookup"><span data-stu-id="994e1-152">OUTPUTS</span></span>

### <span data-ttu-id="994e1-153">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="994e1-153">System.Boolean</span></span>

## <span data-ttu-id="994e1-154">상속자</span><span class="sxs-lookup"><span data-stu-id="994e1-154">NOTES</span></span>

## <span data-ttu-id="994e1-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="994e1-155">RELATED LINKS</span></span>

[<span data-ttu-id="994e1-156">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="994e1-156">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="994e1-157">새로운 AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="994e1-157">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="994e1-158">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="994e1-158">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


