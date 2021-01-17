---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/update-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
ms.openlocfilehash: 160d6b4d4a8505c99d5bfcb4c535ec7bbb3b6dd3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335073"
---
# <span data-ttu-id="3d4a4-101">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="3d4a4-101">Update-AzSupportTicket</span></span>

## <span data-ttu-id="3d4a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d4a4-102">SYNOPSIS</span></span>
<span data-ttu-id="3d4a4-103">지원 티켓을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-103">Updates support ticket.</span></span>

## <span data-ttu-id="3d4a4-104">구문</span><span class="sxs-lookup"><span data-stu-id="3d4a4-104">SYNTAX</span></span>

### <span data-ttu-id="3d4a4-105">UpdateByNameWithContactDetailParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3d4a4-105">UpdateByNameWithContactDetailParameterSet (Default)</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d4a4-106">UpdateByNameWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d4a4-106">UpdateByNameWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] -CustomerContactDetail <PSContactProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d4a4-107">UpdateByInputObjectWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d4a4-107">UpdateByInputObjectWithContactDetailParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d4a4-108">UpdateByInputObjectWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d4a4-108">UpdateByInputObjectWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>]
 -CustomerContactDetail <PSContactProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d4a4-109">설명</span><span class="sxs-lookup"><span data-stu-id="3d4a4-109">DESCRIPTION</span></span>
<span data-ttu-id="3d4a4-110">이 cmdlet을 사용하여 지원 티켓의 심각도 수준, 상태 또는 고객 연락처 세부 정보를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-110">Use this cmdlet to update a support ticket's severity level, status or customer contact details.</span></span> <span data-ttu-id="3d4a4-111">티켓이 지원 엔지니어에게 할당된 경우 지원 티켓의 심각도 수준 또는 상태 업데이트가 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-111">Note that updating a support ticket's severity level or status is not allowed when the ticket is assigned to a support engineer.</span></span> <span data-ttu-id="3d4a4-112">티켓 할당 후 심각도 수준 또는 상태를 업데이트할 경우 티켓에 대한 통신을 보내 지원 엔지니어에게 문의하세요.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-112">If you wish to update the severity level or status after ticket assignment, contact the support engineer by sending a communication on the ticket.</span></span>

## <span data-ttu-id="3d4a4-113">예제</span><span class="sxs-lookup"><span data-stu-id="3d4a4-113">EXAMPLES</span></span>

### <span data-ttu-id="3d4a4-114">예제 1: 지원 티켓의 심각도 업데이트</span><span class="sxs-lookup"><span data-stu-id="3d4a4-114">Example 1: Update severity of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="3d4a4-115">예제 2: 지원 티켓의 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-115">Example 2: Update status of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="3d4a4-116">예제 3: 연락처 개체를 지정하여 지원 티켓의 연락처 세부 정보를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-116">Example 3: Update contact details of support ticket by specify contact object.</span></span>
```powershell
PS C:\> $contactDetail = new-object Microsoft.Azure.Commands.Support.Models.PSContactProfile
PS C:\> $contactDetail.FirstName = "first name updated"
PS C:\> $contactDetail.LastName = "last name updated"
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerContactDetail $contactDetail 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="3d4a4-117">예제 4: 지원 티켓 개체를 파이핑하여 지원 티켓의 심각도 업데이트</span><span class="sxs-lookup"><span data-stu-id="3d4a4-117">Example 4: Update severity of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="3d4a4-118">예제 5: 개별 연락처 매개 변수를 지정하여 지원 티켓의 연락처 세부 정보를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-118">Example 5: Update contact details of support ticket by specifying individual contact parameters.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerFirstName "first name updated" -CustomerLastName "last name updated" -AdditionalEmailAddress @("user2@contoso.com") 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="3d4a4-119">예제 6: 지원 티켓 개체를 파이핑하여 지원 티켓의 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-119">Example 6: Update status of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="3d4a4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d4a4-120">PARAMETERS</span></span>

### <span data-ttu-id="3d4a4-121">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3d4a4-121">-AdditionalEmailAddress</span></span>
<span data-ttu-id="3d4a4-122">추가 전자 메일 주소.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-122">Additional email addresses.</span></span>
<span data-ttu-id="3d4a4-123">여기에 나열된 전자 메일 주소는 지원 티켓에 대한 모든 대응에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-123">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4a4-124">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="3d4a4-124">-CustomerContactDetail</span></span>
<span data-ttu-id="3d4a4-125">SupportTicket에서 연락처 세부 정보를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-125">Update Contact details on SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: UpdateByNameWithContactObjectParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4a4-126">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="3d4a4-126">-CustomerCountry</span></span>
<span data-ttu-id="3d4a4-127">고객 국가입니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-127">Customer country.</span></span>
<span data-ttu-id="3d4a4-128">유효한 ISO Alpha-3 국가 코드(ISO 3166)입니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-128">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4a4-129">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="3d4a4-129">-CustomerFirstName</span></span>
<span data-ttu-id="3d4a4-130">고객 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-130">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4a4-131">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="3d4a4-131">-CustomerLastName</span></span>
<span data-ttu-id="3d4a4-132">고객 성입니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-132">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4a4-133">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="3d4a4-133">-CustomerPhoneNumber</span></span>
<span data-ttu-id="3d4a4-134">고객 전화 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-134">Customer phone number.</span></span>
<span data-ttu-id="3d4a4-135">이 방법은 기본 연락 방법이 전화인 경우 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-135">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4a4-136">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="3d4a4-136">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="3d4a4-137">고객이 선호하는 지원 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-137">Customer preferred support language.</span></span>
<span data-ttu-id="3d4a4-138">이 코드는 여기에 나열된 지원되는 언어 중 하나에 대한 유효한 언어 contry https://azure.microsoft.com/support/faq/ 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-138">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4a4-139">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="3d4a4-139">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="3d4a4-140">고객이 선호하는 표준 시간대입니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-140">Customer preferred time zone.</span></span>
<span data-ttu-id="3d4a4-141">이 값은 유효한 System.TimeZoneInfo.Id 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-141">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4a4-142">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3d4a4-142">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="3d4a4-143">고객 기본 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-143">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4a4-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d4a4-144">-DefaultProfile</span></span>
<span data-ttu-id="3d4a4-145">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d4a4-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d4a4-146">-InputObject</span></span>
<span data-ttu-id="3d4a4-147">이 cmdlet이 업데이트하는 SupportTicket 리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-147">SupportTicket resource object that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: UpdateByInputObjectWithContactDetailParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d4a4-148">-Name</span><span class="sxs-lookup"><span data-stu-id="3d4a4-148">-Name</span></span>
<span data-ttu-id="3d4a4-149">이 cmdlet이 업데이트하는 SupportTicket 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-149">Name of SupportTicket resource that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByNameWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4a4-150">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="3d4a4-150">-PreferredContactMethod</span></span>
<span data-ttu-id="3d4a4-151">기본 연락 방법.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-151">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4a4-152">-심각도</span><span class="sxs-lookup"><span data-stu-id="3d4a4-152">-Severity</span></span>
<span data-ttu-id="3d4a4-153">SupportTicket의 심각도 업데이트</span><span class="sxs-lookup"><span data-stu-id="3d4a4-153">Update Severity of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4a4-154">-Status</span><span class="sxs-lookup"><span data-stu-id="3d4a4-154">-Status</span></span>
<span data-ttu-id="3d4a4-155">SupportTicket의 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-155">Update Status of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Status
Parameter Sets: (All)
Aliases:
Accepted values: Open, Closed

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4a4-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d4a4-156">-Confirm</span></span>
<span data-ttu-id="3d4a4-157">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d4a4-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d4a4-158">-WhatIf</span></span>
<span data-ttu-id="3d4a4-159">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3d4a4-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d4a4-160">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d4a4-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d4a4-161">CommonParameters</span></span>
<span data-ttu-id="3d4a4-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d4a4-163">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3d4a4-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d4a4-164">입력</span><span class="sxs-lookup"><span data-stu-id="3d4a4-164">INPUTS</span></span>

### <span data-ttu-id="3d4a4-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="3d4a4-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="3d4a4-166">출력</span><span class="sxs-lookup"><span data-stu-id="3d4a4-166">OUTPUTS</span></span>

### <span data-ttu-id="3d4a4-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="3d4a4-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="3d4a4-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3d4a4-168">NOTES</span></span>

## <span data-ttu-id="3d4a4-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d4a4-169">RELATED LINKS</span></span>
