---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: 97be8f9eef611a87dae045df680d2823dc2f7acb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534691"
---
# <span data-ttu-id="86886-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="86886-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="86886-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86886-102">SYNOPSIS</span></span>
<span data-ttu-id="86886-103">정책 할당을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86886-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86886-104">구문과</span><span class="sxs-lookup"><span data-stu-id="86886-104">SYNTAX</span></span>

### <span data-ttu-id="86886-105">SetByPolicyAssignmentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="86886-105">SetByPolicyAssignmentName (Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="86886-106">SetByPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="86886-106">SetByPolicyAssignmentId</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="86886-107">설명은</span><span class="sxs-lookup"><span data-stu-id="86886-107">DESCRIPTION</span></span>
<span data-ttu-id="86886-108">**Set-AzureRmPolicyAssignment** cmdlet은 정책 할당을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86886-108">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="86886-109">ID 또는 이름 및 범위를 기준으로 과제를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86886-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="86886-110">예제의</span><span class="sxs-lookup"><span data-stu-id="86886-110">EXAMPLES</span></span>

### <span data-ttu-id="86886-111">예제 1: 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="86886-111">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="86886-112">첫 번째 명령은 Get-AzureRMResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86886-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="86886-113">명령이 $ResourceGroup 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="86886-113">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="86886-114">두 번째 명령은 Get-AzureRmPolicyAssignment cmdlet을 사용 하 여 PolicyAssignment 이라는 정책 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86886-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="86886-115">명령이 $PolicyAssignment 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="86886-115">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="86886-116">마지막 명령은 $PolicyAssignment의 **ResourceId** 속성으로 식별 되는 정책 할당의 표시 이름을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="86886-116">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="86886-117">변수</span><span class="sxs-lookup"><span data-stu-id="86886-117">PARAMETERS</span></span>

### <span data-ttu-id="86886-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="86886-118">-ApiVersion</span></span>
<span data-ttu-id="86886-119">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86886-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="86886-120">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="86886-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="86886-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86886-121">-DefaultProfile</span></span>
<span data-ttu-id="86886-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="86886-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86886-123">-설명</span><span class="sxs-lookup"><span data-stu-id="86886-123">-Description</span></span>
<span data-ttu-id="86886-124">정책 할당에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="86886-124">The description for policy assignment</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86886-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="86886-125">-DisplayName</span></span>
<span data-ttu-id="86886-126">정책 할당에 대 한 새 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86886-126">Specifies a new display name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86886-127">-Id</span><span class="sxs-lookup"><span data-stu-id="86886-127">-Id</span></span>
<span data-ttu-id="86886-128">이 cmdlet이 수정 하는 정책 할당에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86886-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86886-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="86886-129">-InformationAction</span></span>
<span data-ttu-id="86886-130">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86886-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="86886-131">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="86886-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="86886-132">하기로</span><span class="sxs-lookup"><span data-stu-id="86886-132">Continue</span></span>
- <span data-ttu-id="86886-133">숨기기</span><span class="sxs-lookup"><span data-stu-id="86886-133">Ignore</span></span>
- <span data-ttu-id="86886-134">Inquire</span><span class="sxs-lookup"><span data-stu-id="86886-134">Inquire</span></span>
- <span data-ttu-id="86886-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="86886-135">SilentlyContinue</span></span>
- <span data-ttu-id="86886-136">중지가</span><span class="sxs-lookup"><span data-stu-id="86886-136">Stop</span></span>
- <span data-ttu-id="86886-137">대기</span><span class="sxs-lookup"><span data-stu-id="86886-137">Suspend</span></span>

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

### <span data-ttu-id="86886-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="86886-138">-InformationVariable</span></span>
<span data-ttu-id="86886-139">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86886-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="86886-140">-이름</span><span class="sxs-lookup"><span data-stu-id="86886-140">-Name</span></span>
<span data-ttu-id="86886-141">이 cmdlet이 수정 하는 정책 할당의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86886-141">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86886-142">-NotScope</span><span class="sxs-lookup"><span data-stu-id="86886-142">-NotScope</span></span>
<span data-ttu-id="86886-143">정책 할당이 범위를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86886-143">The policy assignment not scopes.</span></span>

```yaml
Type: String[]
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86886-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="86886-144">-Pre</span></span>
<span data-ttu-id="86886-145">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="86886-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="86886-146">-범위</span><span class="sxs-lookup"><span data-stu-id="86886-146">-Scope</span></span>
<span data-ttu-id="86886-147">정책이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86886-147">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86886-148">-Sku</span><span class="sxs-lookup"><span data-stu-id="86886-148">-Sku</span></span>
<span data-ttu-id="86886-149">Sku 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="86886-149">A hash table which represents sku properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86886-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86886-150">CommonParameters</span></span>
<span data-ttu-id="86886-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="86886-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86886-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86886-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86886-153">입력</span><span class="sxs-lookup"><span data-stu-id="86886-153">INPUTS</span></span>

### <span data-ttu-id="86886-154">않아야</span><span class="sxs-lookup"><span data-stu-id="86886-154">None</span></span>
<span data-ttu-id="86886-155">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86886-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="86886-156">출력</span><span class="sxs-lookup"><span data-stu-id="86886-156">OUTPUTS</span></span>

### <span data-ttu-id="86886-157">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="86886-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="86886-158">상속자</span><span class="sxs-lookup"><span data-stu-id="86886-158">NOTES</span></span>

## <span data-ttu-id="86886-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86886-159">RELATED LINKS</span></span>

[<span data-ttu-id="86886-160">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="86886-160">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="86886-161">새로운 AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="86886-161">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="86886-162">제거-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="86886-162">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


