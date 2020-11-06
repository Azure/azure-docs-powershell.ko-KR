---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 11a28cb8848c197d9d766b05833e8c0ca3106412
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529161"
---
# <span data-ttu-id="775c9-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="775c9-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="775c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="775c9-102">SYNOPSIS</span></span>
<span data-ttu-id="775c9-103">정책 할당을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="775c9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="775c9-104">SYNTAX</span></span>

### <span data-ttu-id="775c9-105">모든 정책 할당 매개 변수 집합 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-105">The list all policy assignments parameter set.</span></span> <span data-ttu-id="775c9-106">기본값</span><span class="sxs-lookup"><span data-stu-id="775c9-106">(Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="775c9-107">정책 할당 이름 매개 변수 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-107">The policy assignment name parameter set.</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="775c9-108">정책 할당 Id 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="775c9-108">The policy assignment Id parameter set.</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="775c9-109">설명은</span><span class="sxs-lookup"><span data-stu-id="775c9-109">DESCRIPTION</span></span>
<span data-ttu-id="775c9-110">**AzureRmPolicyAssignment** cmdlet은 모든 정책 할당 또는 특정 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="775c9-111">정책 할당을 식별 하 여 이름, 범위 또는 ID로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="775c9-112">예제의</span><span class="sxs-lookup"><span data-stu-id="775c9-112">EXAMPLES</span></span>

### <span data-ttu-id="775c9-113">예제 1: 모든 정책 할당 가져오기</span><span class="sxs-lookup"><span data-stu-id="775c9-113">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="775c9-114">이 명령은 모든 정책 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="775c9-115">예제 2: 특정 정책 할당 가져오기</span><span class="sxs-lookup"><span data-stu-id="775c9-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="775c9-116">첫 번째 명령은 Get-AzureRMResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="775c9-117">명령이 $ResourceGroup 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-117">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="775c9-118">두 번째 명령은 $ResourceGroup의 **ResourceId** 속성이 식별 하는 범위에 대 한 PolicyAssignment07 라는 정책 할당을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-118">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="775c9-119">변수</span><span class="sxs-lookup"><span data-stu-id="775c9-119">PARAMETERS</span></span>

### <span data-ttu-id="775c9-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="775c9-120">-ApiVersion</span></span>
<span data-ttu-id="775c9-121">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="775c9-122">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="775c9-123">-Id</span><span class="sxs-lookup"><span data-stu-id="775c9-123">-Id</span></span>
<span data-ttu-id="775c9-124">이 cmdlet이 가져오는 정책 할당에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-124">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="775c9-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="775c9-125">-InformationAction</span></span>
<span data-ttu-id="775c9-126">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="775c9-127">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="775c9-128">하기로</span><span class="sxs-lookup"><span data-stu-id="775c9-128">Continue</span></span>
- <span data-ttu-id="775c9-129">숨기기</span><span class="sxs-lookup"><span data-stu-id="775c9-129">Ignore</span></span>
- <span data-ttu-id="775c9-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="775c9-130">Inquire</span></span>
- <span data-ttu-id="775c9-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="775c9-131">SilentlyContinue</span></span>
- <span data-ttu-id="775c9-132">중지가</span><span class="sxs-lookup"><span data-stu-id="775c9-132">Stop</span></span>
- <span data-ttu-id="775c9-133">대기</span><span class="sxs-lookup"><span data-stu-id="775c9-133">Suspend</span></span>

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

### <span data-ttu-id="775c9-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="775c9-134">-InformationVariable</span></span>
<span data-ttu-id="775c9-135">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="775c9-136">-이름</span><span class="sxs-lookup"><span data-stu-id="775c9-136">-Name</span></span>
<span data-ttu-id="775c9-137">이 cmdlet이 가져오는 정책 할당의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-137">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="775c9-138">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="775c9-138">-PolicyDefinitionId</span></span>
<span data-ttu-id="775c9-139">이 cmdlet이 가져오는 정책 할당의 정책 정의에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-139">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set., The policy assignment Id parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="775c9-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="775c9-140">-Pre</span></span>
<span data-ttu-id="775c9-141">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="775c9-142">-범위</span><span class="sxs-lookup"><span data-stu-id="775c9-142">-Scope</span></span>
<span data-ttu-id="775c9-143">이 cmdlet이 가져오는 할당에 대해 정책이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-143">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="775c9-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="775c9-144">-DefaultProfile</span></span>
<span data-ttu-id="775c9-145">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="775c9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="775c9-146">CommonParameters</span></span>
<span data-ttu-id="775c9-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="775c9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="775c9-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="775c9-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="775c9-149">입력</span><span class="sxs-lookup"><span data-stu-id="775c9-149">INPUTS</span></span>

## <span data-ttu-id="775c9-150">출력</span><span class="sxs-lookup"><span data-stu-id="775c9-150">OUTPUTS</span></span>

### <span data-ttu-id="775c9-151">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="775c9-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="775c9-152">상속자</span><span class="sxs-lookup"><span data-stu-id="775c9-152">NOTES</span></span>

## <span data-ttu-id="775c9-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="775c9-153">RELATED LINKS</span></span>

[<span data-ttu-id="775c9-154">새로운 AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="775c9-154">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="775c9-155">제거-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="775c9-155">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="775c9-156">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="775c9-156">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


