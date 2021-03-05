---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 5b2dfbc472b128a12f108aafc92aa9d30b661255
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002160"
---
# <span data-ttu-id="a5b81-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="a5b81-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="a5b81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5b81-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b81-103">지원 연락처 프로필 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="a5b81-104">구문</span><span class="sxs-lookup"><span data-stu-id="a5b81-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5b81-105">설명</span><span class="sxs-lookup"><span data-stu-id="a5b81-105">DESCRIPTION</span></span>
<span data-ttu-id="a5b81-106">지원 티켓을 만들거나 업데이트할 때 지원 연락처 프로필 개체를 만드는 데 사용할 수 있는 도우미 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="a5b81-107">지원 티켓을 만드는 데 필수인 다음 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="a5b81-108">예제</span><span class="sxs-lookup"><span data-stu-id="a5b81-108">EXAMPLES</span></span>

### <span data-ttu-id="a5b81-109">예제 1: 연락처 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="a5b81-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="a5b81-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a5b81-110">PARAMETERS</span></span>

### <span data-ttu-id="a5b81-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="a5b81-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="a5b81-112">여기에 나열된 전자 메일 주소는 지원 티켓에 대한 모든 통신에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="a5b81-113">-Country</span><span class="sxs-lookup"><span data-stu-id="a5b81-113">-Country</span></span>
<span data-ttu-id="a5b81-114">고객 국가입니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-114">Customer country.</span></span>
<span data-ttu-id="a5b81-115">유효한 ISO Alpha-3 국가 코드(ISO 3166)입니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="a5b81-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b81-116">-DefaultProfile</span></span>
<span data-ttu-id="a5b81-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b81-118">-FirstName</span><span class="sxs-lookup"><span data-stu-id="a5b81-118">-FirstName</span></span>
<span data-ttu-id="a5b81-119">고객 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-119">Customer first name.</span></span>

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

### <span data-ttu-id="a5b81-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="a5b81-120">-LastName</span></span>
<span data-ttu-id="a5b81-121">고객 성입니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-121">Customer last name.</span></span>

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

### <span data-ttu-id="a5b81-122">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="a5b81-122">-PhoneNumber</span></span>
<span data-ttu-id="a5b81-123">고객 전화 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-123">Customer phone number.</span></span>
<span data-ttu-id="a5b81-124">기본 연락처 메서드가 전화인 경우 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-124">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="a5b81-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="a5b81-125">-PreferredContactMethod</span></span>
<span data-ttu-id="a5b81-126">기본 설정 연락처 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-126">Preferred contact method.</span></span>

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

### <span data-ttu-id="a5b81-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="a5b81-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="a5b81-128">고객이 선호하는 지원 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-128">Customer preferred support language.</span></span>
<span data-ttu-id="a5b81-129">이 코드는 여기에 나열된 지원되는 언어 중 하나에 대한 유효한 언어 contry 코드 되어야 https://azure.microsoft.com/support/faq/ 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="a5b81-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="a5b81-130">-PreferredTimeZone</span></span>
<span data-ttu-id="a5b81-131">고객이 선호하는 표준 시간대입니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-131">Customer preferred time zone.</span></span>
<span data-ttu-id="a5b81-132">이 값은 유효한 System.TimeZoneInfo.Id 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="a5b81-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="a5b81-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="a5b81-134">고객 기본 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-134">Customer primary email address.</span></span>

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

### <span data-ttu-id="a5b81-135">-확인</span><span class="sxs-lookup"><span data-stu-id="a5b81-135">-Confirm</span></span>
<span data-ttu-id="a5b81-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b81-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b81-137">-WhatIf</span></span>
<span data-ttu-id="a5b81-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5b81-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b81-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b81-140">CommonParameters</span></span>
<span data-ttu-id="a5b81-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b81-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b81-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5b81-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b81-143">입력</span><span class="sxs-lookup"><span data-stu-id="a5b81-143">INPUTS</span></span>

### <span data-ttu-id="a5b81-144">없음</span><span class="sxs-lookup"><span data-stu-id="a5b81-144">None</span></span>

## <span data-ttu-id="a5b81-145">출력</span><span class="sxs-lookup"><span data-stu-id="a5b81-145">OUTPUTS</span></span>

### <span data-ttu-id="a5b81-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="a5b81-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="a5b81-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a5b81-147">NOTES</span></span>

## <span data-ttu-id="a5b81-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5b81-148">RELATED LINKS</span></span>
