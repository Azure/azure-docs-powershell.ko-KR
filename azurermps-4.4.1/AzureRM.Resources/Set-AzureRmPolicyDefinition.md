---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: 2404c0f2dc6c357503f23e7ed509f1c58c352c8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710954"
---
# <span data-ttu-id="31636-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="31636-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="31636-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31636-102">SYNOPSIS</span></span>
<span data-ttu-id="31636-103">정책 정의를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31636-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31636-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31636-104">SYNTAX</span></span>

### <span data-ttu-id="31636-105">정책 정의 이름 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="31636-105">The policy definition name parameter set.</span></span> <span data-ttu-id="31636-106">기본값</span><span class="sxs-lookup"><span data-stu-id="31636-106">(Default)</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="31636-107">정책 정의 Id 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="31636-107">The policy definition Id parameter set.</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="31636-108">설명은</span><span class="sxs-lookup"><span data-stu-id="31636-108">DESCRIPTION</span></span>
<span data-ttu-id="31636-109">**Set-AzureRmPolicyDefinition** cmdlet은 정책 정의를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31636-109">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="31636-110">예제의</span><span class="sxs-lookup"><span data-stu-id="31636-110">EXAMPLES</span></span>

### <span data-ttu-id="31636-111">예제 1: 정책 정의에 대 한 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="31636-111">Example 1: Update the description of a policy definition</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
PS C:\> Set-AzureRmPolicyDefinition -Id $Policy.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="31636-112">첫 번째 명령은 Get-AzureRmPolicyDefinition cmdlet을 사용 하 여 VMPolicyDefinition 이라는 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31636-112">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="31636-113">명령이 $PolicyDefinition 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="31636-113">The command stores that object in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="31636-114">두 번째 명령은 $PolicyDefinition의 **ResourceId** 속성으로 식별 되는 정책 정의에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="31636-114">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="31636-115">변수</span><span class="sxs-lookup"><span data-stu-id="31636-115">PARAMETERS</span></span>

### <span data-ttu-id="31636-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="31636-116">-ApiVersion</span></span>
<span data-ttu-id="31636-117">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31636-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="31636-118">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="31636-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="31636-119">-설명</span><span class="sxs-lookup"><span data-stu-id="31636-119">-Description</span></span>
<span data-ttu-id="31636-120">정책 정의에 대 한 새 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31636-120">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="31636-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="31636-121">-DisplayName</span></span>
<span data-ttu-id="31636-122">정책 정의에 대 한 새 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31636-122">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="31636-123">-Id</span><span class="sxs-lookup"><span data-stu-id="31636-123">-Id</span></span>
<span data-ttu-id="31636-124">이 cmdlet이 수정 하는 정책 정의에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31636-124">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="31636-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="31636-125">-InformationAction</span></span>
<span data-ttu-id="31636-126">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31636-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="31636-127">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="31636-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="31636-128">하기로</span><span class="sxs-lookup"><span data-stu-id="31636-128">Continue</span></span>
- <span data-ttu-id="31636-129">숨기기</span><span class="sxs-lookup"><span data-stu-id="31636-129">Ignore</span></span>
- <span data-ttu-id="31636-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="31636-130">Inquire</span></span>
- <span data-ttu-id="31636-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="31636-131">SilentlyContinue</span></span>
- <span data-ttu-id="31636-132">중지가</span><span class="sxs-lookup"><span data-stu-id="31636-132">Stop</span></span>
- <span data-ttu-id="31636-133">대기</span><span class="sxs-lookup"><span data-stu-id="31636-133">Suspend</span></span>

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

### <span data-ttu-id="31636-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="31636-134">-InformationVariable</span></span>
<span data-ttu-id="31636-135">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31636-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="31636-136">-이름</span><span class="sxs-lookup"><span data-stu-id="31636-136">-Name</span></span>
<span data-ttu-id="31636-137">이 cmdlet이 수정 하는 정책 정의의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31636-137">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="31636-138">-정책</span><span class="sxs-lookup"><span data-stu-id="31636-138">-Policy</span></span>
<span data-ttu-id="31636-139">정책 정의에 대 한 새 정책 규칙을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31636-139">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="31636-140">Json 파일의 경로 또는 JSON (JavaScript Object Notation) 형식의 정책을 포함 하는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31636-140">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="31636-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="31636-141">-Pre</span></span>
<span data-ttu-id="31636-142">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="31636-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="31636-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31636-143">-DefaultProfile</span></span>
<span data-ttu-id="31636-144">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31636-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31636-145">-Metadata</span><span class="sxs-lookup"><span data-stu-id="31636-145">-Metadata</span></span>
<span data-ttu-id="31636-146">정책 정의에 대 한 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="31636-146">The metadata for policy definition.</span></span> <span data-ttu-id="31636-147">메타 데이터를 포함 하는 파일 이름에 대 한 경로 이거나 메타 데이터 인 string 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31636-147">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="31636-148">-Parameter</span><span class="sxs-lookup"><span data-stu-id="31636-148">-Parameter</span></span>
<span data-ttu-id="31636-149">정책 정의에 대 한 매개 변수 선언입니다.</span><span class="sxs-lookup"><span data-stu-id="31636-149">The parameters declaration for policy definition.</span></span> <span data-ttu-id="31636-150">매개 변수 선언을 포함 하는 uri 또는 파일 이름 또는 매개 변수 선언 문자열의 경로일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31636-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="31636-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31636-151">CommonParameters</span></span>
<span data-ttu-id="31636-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31636-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31636-153">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31636-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31636-154">입력</span><span class="sxs-lookup"><span data-stu-id="31636-154">INPUTS</span></span>

## <span data-ttu-id="31636-155">출력</span><span class="sxs-lookup"><span data-stu-id="31636-155">OUTPUTS</span></span>

### <span data-ttu-id="31636-156">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="31636-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="31636-157">상속자</span><span class="sxs-lookup"><span data-stu-id="31636-157">NOTES</span></span>

## <span data-ttu-id="31636-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31636-158">RELATED LINKS</span></span>

[<span data-ttu-id="31636-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="31636-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="31636-160">새로운 AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="31636-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="31636-161">제거-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="31636-161">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


