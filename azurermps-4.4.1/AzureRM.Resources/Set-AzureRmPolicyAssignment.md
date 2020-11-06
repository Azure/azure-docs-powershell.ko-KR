---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: fcb1283531b35365cc8c07016c839a1152011160
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529159"
---
# <span data-ttu-id="30687-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="30687-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="30687-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30687-102">SYNOPSIS</span></span>
<span data-ttu-id="30687-103">정책 할당을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30687-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30687-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30687-104">SYNTAX</span></span>

### <span data-ttu-id="30687-105">정책 할당 이름 매개 변수 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="30687-105">The policy assignment name parameter set.</span></span> <span data-ttu-id="30687-106">기본값</span><span class="sxs-lookup"><span data-stu-id="30687-106">(Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="30687-107">정책 할당 Id 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="30687-107">The policy assignment Id parameter set.</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="30687-108">설명은</span><span class="sxs-lookup"><span data-stu-id="30687-108">DESCRIPTION</span></span>
<span data-ttu-id="30687-109">**Set-AzureRmPolicyAssignment** cmdlet은 정책 할당을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30687-109">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="30687-110">ID 또는 이름 및 범위를 기준으로 과제를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30687-110">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="30687-111">예제의</span><span class="sxs-lookup"><span data-stu-id="30687-111">EXAMPLES</span></span>

### <span data-ttu-id="30687-112">예제 1: 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="30687-112">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="30687-113">첫 번째 명령은 Get-AzureRMResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30687-113">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="30687-114">명령이 $ResourceGroup 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="30687-114">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="30687-115">두 번째 명령은 Get-AzureRmPolicyAssignment cmdlet을 사용 하 여 PolicyAssignment 이라는 정책 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30687-115">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="30687-116">명령이 $PolicyAssignment 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="30687-116">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="30687-117">마지막 명령은 $PolicyAssignment의 **ResourceId** 속성으로 식별 되는 정책 할당의 표시 이름을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="30687-117">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="30687-118">변수</span><span class="sxs-lookup"><span data-stu-id="30687-118">PARAMETERS</span></span>

### <span data-ttu-id="30687-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="30687-119">-ApiVersion</span></span>
<span data-ttu-id="30687-120">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30687-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="30687-121">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="30687-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="30687-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="30687-122">-DisplayName</span></span>
<span data-ttu-id="30687-123">정책 할당에 대 한 새 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30687-123">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="30687-124">-Id</span><span class="sxs-lookup"><span data-stu-id="30687-124">-Id</span></span>
<span data-ttu-id="30687-125">이 cmdlet이 수정 하는 정책 할당에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30687-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30687-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="30687-126">-InformationAction</span></span>
<span data-ttu-id="30687-127">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30687-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="30687-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="30687-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="30687-129">하기로</span><span class="sxs-lookup"><span data-stu-id="30687-129">Continue</span></span>
- <span data-ttu-id="30687-130">숨기기</span><span class="sxs-lookup"><span data-stu-id="30687-130">Ignore</span></span>
- <span data-ttu-id="30687-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="30687-131">Inquire</span></span>
- <span data-ttu-id="30687-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="30687-132">SilentlyContinue</span></span>
- <span data-ttu-id="30687-133">중지가</span><span class="sxs-lookup"><span data-stu-id="30687-133">Stop</span></span>
- <span data-ttu-id="30687-134">대기</span><span class="sxs-lookup"><span data-stu-id="30687-134">Suspend</span></span>

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

### <span data-ttu-id="30687-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="30687-135">-InformationVariable</span></span>
<span data-ttu-id="30687-136">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30687-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="30687-137">-이름</span><span class="sxs-lookup"><span data-stu-id="30687-137">-Name</span></span>
<span data-ttu-id="30687-138">이 cmdlet이 수정 하는 정책 할당의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30687-138">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30687-139">-NotScope</span><span class="sxs-lookup"><span data-stu-id="30687-139">-NotScope</span></span>
<span data-ttu-id="30687-140">정책 할당이 범위를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30687-140">The policy assignment not scopes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30687-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="30687-141">-Pre</span></span>
<span data-ttu-id="30687-142">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="30687-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="30687-143">-범위</span><span class="sxs-lookup"><span data-stu-id="30687-143">-Scope</span></span>
<span data-ttu-id="30687-144">정책이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30687-144">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30687-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30687-145">-DefaultProfile</span></span>
<span data-ttu-id="30687-146">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30687-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30687-147">-설명</span><span class="sxs-lookup"><span data-stu-id="30687-147">-Description</span></span>
<span data-ttu-id="30687-148">정책 할당에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="30687-148">The description for policy assignment.</span></span>

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

### <span data-ttu-id="30687-149">-Sku</span><span class="sxs-lookup"><span data-stu-id="30687-149">-Sku</span></span>
<span data-ttu-id="30687-150">Sku 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="30687-150">A hash table which represents sku properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30687-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30687-151">CommonParameters</span></span>
<span data-ttu-id="30687-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30687-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30687-153">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30687-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30687-154">입력</span><span class="sxs-lookup"><span data-stu-id="30687-154">INPUTS</span></span>

## <span data-ttu-id="30687-155">출력</span><span class="sxs-lookup"><span data-stu-id="30687-155">OUTPUTS</span></span>

### <span data-ttu-id="30687-156">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="30687-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="30687-157">상속자</span><span class="sxs-lookup"><span data-stu-id="30687-157">NOTES</span></span>

## <span data-ttu-id="30687-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30687-158">RELATED LINKS</span></span>

[<span data-ttu-id="30687-159">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="30687-159">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="30687-160">새로운 AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="30687-160">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="30687-161">제거-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="30687-161">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


