---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: d9d79374e426c6d895fbfcef957da20ed9721f70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533655"
---
# <span data-ttu-id="cf443-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cf443-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="cf443-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf443-102">SYNOPSIS</span></span>
<span data-ttu-id="cf443-103">정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf443-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cf443-104">SYNTAX</span></span>

### <span data-ttu-id="cf443-105">GetAllPolicyDefinitions (기본값)</span><span class="sxs-lookup"><span data-stu-id="cf443-105">GetAllPolicyDefinitions (Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cf443-106">GetByPolicyDefintionName</span><span class="sxs-lookup"><span data-stu-id="cf443-106">GetByPolicyDefintionName</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cf443-107">GetByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="cf443-107">GetByPolicyDefinitionId</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cf443-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cf443-108">DESCRIPTION</span></span>
<span data-ttu-id="cf443-109">**AzureRmPolicyDefinition** cmdlet은 이름 또는 ID로 식별 되는 특정 정책 정의 또는 모든 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-109">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="cf443-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cf443-110">EXAMPLES</span></span>

### <span data-ttu-id="cf443-111">예제 1: 모든 정책 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="cf443-111">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="cf443-112">이 명령은 모든 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-112">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="cf443-113">예제 2: 이름별로 정책 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="cf443-113">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="cf443-114">이 명령은 VMPolicyDefinition 이라는 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-114">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="cf443-115">변수</span><span class="sxs-lookup"><span data-stu-id="cf443-115">PARAMETERS</span></span>

### <span data-ttu-id="cf443-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cf443-116">-ApiVersion</span></span>
<span data-ttu-id="cf443-117">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="cf443-118">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="cf443-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf443-119">-DefaultProfile</span></span>
<span data-ttu-id="cf443-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cf443-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf443-121">-Id</span><span class="sxs-lookup"><span data-stu-id="cf443-121">-Id</span></span>
<span data-ttu-id="cf443-122">이 cmdlet이 가져오는 정책 정의에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-122">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf443-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="cf443-123">-InformationAction</span></span>
<span data-ttu-id="cf443-124">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cf443-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cf443-126">하기로</span><span class="sxs-lookup"><span data-stu-id="cf443-126">Continue</span></span>
- <span data-ttu-id="cf443-127">숨기기</span><span class="sxs-lookup"><span data-stu-id="cf443-127">Ignore</span></span>
- <span data-ttu-id="cf443-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="cf443-128">Inquire</span></span>
- <span data-ttu-id="cf443-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cf443-129">SilentlyContinue</span></span>
- <span data-ttu-id="cf443-130">중지가</span><span class="sxs-lookup"><span data-stu-id="cf443-130">Stop</span></span>
- <span data-ttu-id="cf443-131">대기</span><span class="sxs-lookup"><span data-stu-id="cf443-131">Suspend</span></span>

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

### <span data-ttu-id="cf443-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cf443-132">-InformationVariable</span></span>
<span data-ttu-id="cf443-133">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cf443-134">-이름</span><span class="sxs-lookup"><span data-stu-id="cf443-134">-Name</span></span>
<span data-ttu-id="cf443-135">이 cmdlet이 가져오는 정책 정의의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-135">Specifies the name of the policy definition that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefintionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf443-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="cf443-136">-Pre</span></span>
<span data-ttu-id="cf443-137">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cf443-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf443-138">CommonParameters</span></span>
<span data-ttu-id="cf443-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf443-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf443-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf443-141">입력</span><span class="sxs-lookup"><span data-stu-id="cf443-141">INPUTS</span></span>

### <span data-ttu-id="cf443-142">않아야</span><span class="sxs-lookup"><span data-stu-id="cf443-142">None</span></span>
<span data-ttu-id="cf443-143">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cf443-144">출력</span><span class="sxs-lookup"><span data-stu-id="cf443-144">OUTPUTS</span></span>

### <span data-ttu-id="cf443-145">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="cf443-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="cf443-146">상속자</span><span class="sxs-lookup"><span data-stu-id="cf443-146">NOTES</span></span>

## <span data-ttu-id="cf443-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf443-147">RELATED LINKS</span></span>

[<span data-ttu-id="cf443-148">새로운 AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cf443-148">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="cf443-149">제거-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cf443-149">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="cf443-150">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cf443-150">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


