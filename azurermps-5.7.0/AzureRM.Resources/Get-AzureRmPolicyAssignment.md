---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 0604c7bd8f4f016f908eb7e9c93ff6b9d95db979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703552"
---
# <span data-ttu-id="dea86-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dea86-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="dea86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dea86-102">SYNOPSIS</span></span>
<span data-ttu-id="dea86-103">정책 할당을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dea86-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dea86-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dea86-104">SYNTAX</span></span>

### <span data-ttu-id="dea86-105">GetAllPolicyAssignments (기본값)</span><span class="sxs-lookup"><span data-stu-id="dea86-105">GetAllPolicyAssignments (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dea86-106">GetPolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="dea86-106">GetPolicyAssignmentName</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dea86-107">GetPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="dea86-107">GetPolicyAssignmentId</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="dea86-108">설명은</span><span class="sxs-lookup"><span data-stu-id="dea86-108">DESCRIPTION</span></span>
<span data-ttu-id="dea86-109">**AzureRmPolicyAssignment** cmdlet은 모든 정책 할당 또는 특정 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dea86-109">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="dea86-110">정책 할당을 식별 하 여 이름, 범위 또는 ID로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dea86-110">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="dea86-111">예제의</span><span class="sxs-lookup"><span data-stu-id="dea86-111">EXAMPLES</span></span>

### <span data-ttu-id="dea86-112">예제 1: 모든 정책 할당 가져오기</span><span class="sxs-lookup"><span data-stu-id="dea86-112">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="dea86-113">이 명령은 모든 정책 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dea86-113">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="dea86-114">예제 2: 특정 정책 할당 가져오기</span><span class="sxs-lookup"><span data-stu-id="dea86-114">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="dea86-115">첫 번째 명령은 Get-AzureRMResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dea86-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="dea86-116">명령이 $ResourceGroup 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="dea86-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="dea86-117">두 번째 명령은 $ResourceGroup의 **ResourceId** 속성이 식별 하는 범위에 대 한 PolicyAssignment07 라는 정책 할당을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dea86-117">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="dea86-118">변수</span><span class="sxs-lookup"><span data-stu-id="dea86-118">PARAMETERS</span></span>

### <span data-ttu-id="dea86-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dea86-119">-ApiVersion</span></span>
<span data-ttu-id="dea86-120">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dea86-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="dea86-121">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dea86-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="dea86-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dea86-122">-DefaultProfile</span></span>
<span data-ttu-id="dea86-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dea86-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dea86-124">-Id</span><span class="sxs-lookup"><span data-stu-id="dea86-124">-Id</span></span>
<span data-ttu-id="dea86-125">이 cmdlet이 가져오는 정책 할당에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dea86-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dea86-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dea86-126">-InformationAction</span></span>
<span data-ttu-id="dea86-127">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dea86-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dea86-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="dea86-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dea86-129">하기로</span><span class="sxs-lookup"><span data-stu-id="dea86-129">Continue</span></span>
- <span data-ttu-id="dea86-130">숨기기</span><span class="sxs-lookup"><span data-stu-id="dea86-130">Ignore</span></span>
- <span data-ttu-id="dea86-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="dea86-131">Inquire</span></span>
- <span data-ttu-id="dea86-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dea86-132">SilentlyContinue</span></span>
- <span data-ttu-id="dea86-133">중지가</span><span class="sxs-lookup"><span data-stu-id="dea86-133">Stop</span></span>
- <span data-ttu-id="dea86-134">대기</span><span class="sxs-lookup"><span data-stu-id="dea86-134">Suspend</span></span>

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

### <span data-ttu-id="dea86-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dea86-135">-InformationVariable</span></span>
<span data-ttu-id="dea86-136">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dea86-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="dea86-137">-이름</span><span class="sxs-lookup"><span data-stu-id="dea86-137">-Name</span></span>
<span data-ttu-id="dea86-138">이 cmdlet이 가져오는 정책 할당의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dea86-138">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dea86-139">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="dea86-139">-PolicyDefinitionId</span></span>
<span data-ttu-id="dea86-140">이 cmdlet이 가져오는 정책 할당의 정책 정의에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dea86-140">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName, GetPolicyAssignmentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dea86-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="dea86-141">-Pre</span></span>
<span data-ttu-id="dea86-142">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dea86-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="dea86-143">-범위</span><span class="sxs-lookup"><span data-stu-id="dea86-143">-Scope</span></span>
<span data-ttu-id="dea86-144">이 cmdlet이 가져오는 할당에 대해 정책이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dea86-144">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dea86-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dea86-145">CommonParameters</span></span>
<span data-ttu-id="dea86-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dea86-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dea86-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dea86-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dea86-148">입력</span><span class="sxs-lookup"><span data-stu-id="dea86-148">INPUTS</span></span>

### <span data-ttu-id="dea86-149">않아야</span><span class="sxs-lookup"><span data-stu-id="dea86-149">None</span></span>
<span data-ttu-id="dea86-150">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dea86-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dea86-151">출력</span><span class="sxs-lookup"><span data-stu-id="dea86-151">OUTPUTS</span></span>

### <span data-ttu-id="dea86-152">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="dea86-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="dea86-153">상속자</span><span class="sxs-lookup"><span data-stu-id="dea86-153">NOTES</span></span>

## <span data-ttu-id="dea86-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dea86-154">RELATED LINKS</span></span>

[<span data-ttu-id="dea86-155">새로운 AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dea86-155">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="dea86-156">제거-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dea86-156">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="dea86-157">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dea86-157">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


