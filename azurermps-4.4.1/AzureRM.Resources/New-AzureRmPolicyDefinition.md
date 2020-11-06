---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: 5140219c5392a7fb9c727998ae248d600edfde23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533872"
---
# <span data-ttu-id="d24db-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d24db-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="d24db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d24db-102">SYNOPSIS</span></span>
<span data-ttu-id="d24db-103">정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d24db-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d24db-104">SYNTAX</span></span>

```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d24db-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d24db-105">DESCRIPTION</span></span>
<span data-ttu-id="d24db-106">**AzureRmPolicyDefinition** CMDLET은 JSON (JavaScript 개체 표기) 형식의 정책 규칙을 포함 하는 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-106">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="d24db-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d24db-107">EXAMPLES</span></span>

### <span data-ttu-id="d24db-108">예제 1: 정책 파일을 사용 하 여 정책 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="d24db-108">Example 1: Create a policy definition by using a policy file</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -Policy C:\VMPolicy.json
```

<span data-ttu-id="d24db-109">이 명령은 C:\VMPolicy.js에 지정 된 정책 규칙을 포함 하는 VMPolicyDefinition 이라는 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-109">This command creates a policy definition named VMPolicyDefinition that contains the policy rule specified in C:\VMPolicy.json.</span></span>

### <span data-ttu-id="d24db-110">예제 2: 정책 정의 인라인 만들기</span><span class="sxs-lookup"><span data-stu-id="d24db-110">Example 2: Create a policy definition inline</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -DisplayName "Virtual Machine policy definition" -Policy "{""if"":{""source"":""action"",""equals"":""Microsoft.Compute/virtualMachines/write""},""then"":{""effect"":""deny""}}"
```

<span data-ttu-id="d24db-111">이 명령은 VMPolicyDefinition 이라는 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-111">This command creates a policy definition named VMPolicyDefinition.</span></span>
<span data-ttu-id="d24db-112">명령은 정책을 유효한 JSON 형식의 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-112">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="d24db-113">변수</span><span class="sxs-lookup"><span data-stu-id="d24db-113">PARAMETERS</span></span>

### <span data-ttu-id="d24db-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d24db-114">-ApiVersion</span></span>
<span data-ttu-id="d24db-115">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d24db-116">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d24db-117">-설명</span><span class="sxs-lookup"><span data-stu-id="d24db-117">-Description</span></span>
<span data-ttu-id="d24db-118">정책 정의에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-118">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="d24db-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d24db-119">-DisplayName</span></span>
<span data-ttu-id="d24db-120">정책 정의의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-120">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="d24db-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d24db-121">-InformationAction</span></span>
<span data-ttu-id="d24db-122">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d24db-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d24db-124">하기로</span><span class="sxs-lookup"><span data-stu-id="d24db-124">Continue</span></span>
- <span data-ttu-id="d24db-125">숨기기</span><span class="sxs-lookup"><span data-stu-id="d24db-125">Ignore</span></span>
- <span data-ttu-id="d24db-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="d24db-126">Inquire</span></span>
- <span data-ttu-id="d24db-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d24db-127">SilentlyContinue</span></span>
- <span data-ttu-id="d24db-128">중지가</span><span class="sxs-lookup"><span data-stu-id="d24db-128">Stop</span></span>
- <span data-ttu-id="d24db-129">대기</span><span class="sxs-lookup"><span data-stu-id="d24db-129">Suspend</span></span>

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

### <span data-ttu-id="d24db-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d24db-130">-InformationVariable</span></span>
<span data-ttu-id="d24db-131">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d24db-132">-이름</span><span class="sxs-lookup"><span data-stu-id="d24db-132">-Name</span></span>
<span data-ttu-id="d24db-133">정책 정의의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-133">Specifies a name for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d24db-134">-Parameter</span><span class="sxs-lookup"><span data-stu-id="d24db-134">-Parameter</span></span>
<span data-ttu-id="d24db-135">정책 정의에 대 한 매개 변수 선언입니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-135">The parameters declaration for policy definition.</span></span> <span data-ttu-id="d24db-136">매개 변수 선언이 포함 된 파일 이름의 경로 이거나 매개 변수 선언이 string 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="d24db-137">-정책</span><span class="sxs-lookup"><span data-stu-id="d24db-137">-Policy</span></span>
<span data-ttu-id="d24db-138">정책 정의에 대 한 정책 규칙을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-138">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="d24db-139">Json 파일의 경로 또는 정책 (JSON 형식)을 포함 하는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-139">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d24db-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="d24db-140">-Pre</span></span>
<span data-ttu-id="d24db-141">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d24db-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d24db-142">-DefaultProfile</span></span>
<span data-ttu-id="d24db-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d24db-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d24db-144">-Metadata</span></span>
<span data-ttu-id="d24db-145">정책 정의에 대 한 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-145">The metadata for policy definition.</span></span> <span data-ttu-id="d24db-146">메타 데이터를 포함 하는 파일 이름에 대 한 경로 이거나 메타 데이터 인 string 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-146">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="d24db-147">-모드</span><span class="sxs-lookup"><span data-stu-id="d24db-147">-Mode</span></span>
<span data-ttu-id="d24db-148">정책 정의의 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-148">The mode of the policy definition.</span></span>

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

### <span data-ttu-id="d24db-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d24db-149">CommonParameters</span></span>
<span data-ttu-id="d24db-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d24db-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d24db-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d24db-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d24db-152">입력</span><span class="sxs-lookup"><span data-stu-id="d24db-152">INPUTS</span></span>

## <span data-ttu-id="d24db-153">출력</span><span class="sxs-lookup"><span data-stu-id="d24db-153">OUTPUTS</span></span>

### <span data-ttu-id="d24db-154">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="d24db-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d24db-155">상속자</span><span class="sxs-lookup"><span data-stu-id="d24db-155">NOTES</span></span>

## <span data-ttu-id="d24db-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d24db-156">RELATED LINKS</span></span>

[<span data-ttu-id="d24db-157">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d24db-157">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="d24db-158">제거-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d24db-158">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="d24db-159">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d24db-159">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


