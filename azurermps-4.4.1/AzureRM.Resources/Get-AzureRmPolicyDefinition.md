---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: 63ab8e9004b993429af31cb54e360c0b6d9854fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535447"
---
# <span data-ttu-id="6f812-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6f812-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="6f812-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f812-102">SYNOPSIS</span></span>
<span data-ttu-id="6f812-103">정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f812-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f812-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f812-104">SYNTAX</span></span>

### <span data-ttu-id="6f812-105">모든 정책 정의 매개 변수 집합 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6f812-105">The list all policy definitions parameter set.</span></span> <span data-ttu-id="6f812-106">기본값</span><span class="sxs-lookup"><span data-stu-id="6f812-106">(Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6f812-107">정책 정의 이름 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="6f812-107">The policy definition name parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6f812-108">정책 정의 Id 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="6f812-108">The policy definition Id parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6f812-109">설명은</span><span class="sxs-lookup"><span data-stu-id="6f812-109">DESCRIPTION</span></span>
<span data-ttu-id="6f812-110">**AzureRmPolicyDefinition** cmdlet은 이름 또는 ID로 식별 되는 특정 정책 정의 또는 모든 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f812-110">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="6f812-111">예제의</span><span class="sxs-lookup"><span data-stu-id="6f812-111">EXAMPLES</span></span>

### <span data-ttu-id="6f812-112">예제 1: 모든 정책 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="6f812-112">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="6f812-113">이 명령은 모든 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f812-113">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="6f812-114">예제 2: 이름별로 정책 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="6f812-114">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="6f812-115">이 명령은 VMPolicyDefinition 이라는 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f812-115">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="6f812-116">변수</span><span class="sxs-lookup"><span data-stu-id="6f812-116">PARAMETERS</span></span>

### <span data-ttu-id="6f812-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6f812-117">-ApiVersion</span></span>
<span data-ttu-id="6f812-118">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f812-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6f812-119">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f812-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6f812-120">-Id</span><span class="sxs-lookup"><span data-stu-id="6f812-120">-Id</span></span>
<span data-ttu-id="6f812-121">이 cmdlet이 가져오는 정책 정의에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f812-121">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f812-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6f812-122">-InformationAction</span></span>
<span data-ttu-id="6f812-123">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f812-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6f812-124">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6f812-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6f812-125">하기로</span><span class="sxs-lookup"><span data-stu-id="6f812-125">Continue</span></span>
- <span data-ttu-id="6f812-126">숨기기</span><span class="sxs-lookup"><span data-stu-id="6f812-126">Ignore</span></span>
- <span data-ttu-id="6f812-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="6f812-127">Inquire</span></span>
- <span data-ttu-id="6f812-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6f812-128">SilentlyContinue</span></span>
- <span data-ttu-id="6f812-129">중지가</span><span class="sxs-lookup"><span data-stu-id="6f812-129">Stop</span></span>
- <span data-ttu-id="6f812-130">대기</span><span class="sxs-lookup"><span data-stu-id="6f812-130">Suspend</span></span>

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

### <span data-ttu-id="6f812-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6f812-131">-InformationVariable</span></span>
<span data-ttu-id="6f812-132">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f812-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6f812-133">-이름</span><span class="sxs-lookup"><span data-stu-id="6f812-133">-Name</span></span>
<span data-ttu-id="6f812-134">이 cmdlet이 가져오는 정책 정의의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f812-134">Specifies the name of the policy definition that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f812-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="6f812-135">-Pre</span></span>
<span data-ttu-id="6f812-136">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6f812-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6f812-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f812-137">-DefaultProfile</span></span>
<span data-ttu-id="6f812-138">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f812-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f812-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f812-139">CommonParameters</span></span>
<span data-ttu-id="6f812-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f812-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f812-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f812-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f812-142">입력</span><span class="sxs-lookup"><span data-stu-id="6f812-142">INPUTS</span></span>

## <span data-ttu-id="6f812-143">출력</span><span class="sxs-lookup"><span data-stu-id="6f812-143">OUTPUTS</span></span>

### <span data-ttu-id="6f812-144">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="6f812-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6f812-145">상속자</span><span class="sxs-lookup"><span data-stu-id="6f812-145">NOTES</span></span>

## <span data-ttu-id="6f812-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f812-146">RELATED LINKS</span></span>

[<span data-ttu-id="6f812-147">새로운 AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6f812-147">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="6f812-148">제거-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6f812-148">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="6f812-149">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6f812-149">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


