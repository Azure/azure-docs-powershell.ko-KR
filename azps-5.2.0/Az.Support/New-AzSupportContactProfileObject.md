---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 312fa24c8805664867d86bdaf38a01d287a3c499
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362097"
---
# <span data-ttu-id="91821-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="91821-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="91821-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91821-102">SYNOPSIS</span></span>
<span data-ttu-id="91821-103">지원 연락처 프로필 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91821-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="91821-104">구문</span><span class="sxs-lookup"><span data-stu-id="91821-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91821-105">설명</span><span class="sxs-lookup"><span data-stu-id="91821-105">DESCRIPTION</span></span>
<span data-ttu-id="91821-106">지원 티켓을 만들거나 업데이트할 때 지원 연락처 프로필 개체를 만드는 데 사용할 수 있는 도우미 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="91821-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="91821-107">지원 티켓을 만드는 데 필수인 다음 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91821-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="91821-108">예제</span><span class="sxs-lookup"><span data-stu-id="91821-108">EXAMPLES</span></span>

### <span data-ttu-id="91821-109">예제 1: 연락처 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="91821-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="91821-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91821-110">PARAMETERS</span></span>

### <span data-ttu-id="91821-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="91821-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="91821-112">여기에 나열된 전자 메일 주소는 지원 티켓에 대한 모든 대응에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="91821-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91821-113">-Country</span><span class="sxs-lookup"><span data-stu-id="91821-113">-Country</span></span>
<span data-ttu-id="91821-114">고객 국가입니다.</span><span class="sxs-lookup"><span data-stu-id="91821-114">Customer country.</span></span>
<span data-ttu-id="91821-115">유효한 ISO Alpha-3 국가 코드(ISO 3166)입니다.</span><span class="sxs-lookup"><span data-stu-id="91821-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91821-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91821-116">-DefaultProfile</span></span>
<span data-ttu-id="91821-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91821-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91821-118">-FirstName</span><span class="sxs-lookup"><span data-stu-id="91821-118">-FirstName</span></span>
<span data-ttu-id="91821-119">고객 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91821-119">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91821-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="91821-120">-LastName</span></span>
<span data-ttu-id="91821-121">고객 성입니다.</span><span class="sxs-lookup"><span data-stu-id="91821-121">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91821-122">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="91821-122">-PhoneNumber</span></span>
<span data-ttu-id="91821-123">고객 전화 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="91821-123">Customer phone number.</span></span>
<span data-ttu-id="91821-124">이 방법은 기본 연락 방법이 전화인 경우 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="91821-124">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="91821-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="91821-125">-PreferredContactMethod</span></span>
<span data-ttu-id="91821-126">기본 연락 방법.</span><span class="sxs-lookup"><span data-stu-id="91821-126">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: (All)
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91821-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="91821-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="91821-128">고객이 선호하는 지원 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="91821-128">Customer preferred support language.</span></span>
<span data-ttu-id="91821-129">이 코드는 여기에 나열된 지원되는 언어 중 하나에 대한 유효한 언어 contry https://azure.microsoft.com/support/faq/ 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="91821-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91821-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="91821-130">-PreferredTimeZone</span></span>
<span data-ttu-id="91821-131">고객이 선호하는 표준 시간대입니다.</span><span class="sxs-lookup"><span data-stu-id="91821-131">Customer preferred time zone.</span></span>
<span data-ttu-id="91821-132">이 값은 유효한 System.TimeZoneInfo.Id 합니다.</span><span class="sxs-lookup"><span data-stu-id="91821-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91821-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="91821-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="91821-134">고객 기본 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="91821-134">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91821-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91821-135">-Confirm</span></span>
<span data-ttu-id="91821-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="91821-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91821-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91821-137">-WhatIf</span></span>
<span data-ttu-id="91821-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="91821-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91821-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91821-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91821-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91821-140">CommonParameters</span></span>
<span data-ttu-id="91821-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="91821-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91821-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="91821-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91821-143">입력</span><span class="sxs-lookup"><span data-stu-id="91821-143">INPUTS</span></span>

### <span data-ttu-id="91821-144">없음</span><span class="sxs-lookup"><span data-stu-id="91821-144">None</span></span>

## <span data-ttu-id="91821-145">출력</span><span class="sxs-lookup"><span data-stu-id="91821-145">OUTPUTS</span></span>

### <span data-ttu-id="91821-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="91821-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="91821-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="91821-147">NOTES</span></span>

## <span data-ttu-id="91821-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91821-148">RELATED LINKS</span></span>
