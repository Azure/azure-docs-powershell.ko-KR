---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/update-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
ms.openlocfilehash: 160d6b4d4a8505c99d5bfcb4c535ec7bbb3b6dd3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217150"
---
# <span data-ttu-id="770b2-101">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="770b2-101">Update-AzSupportTicket</span></span>

## <span data-ttu-id="770b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="770b2-102">SYNOPSIS</span></span>
<span data-ttu-id="770b2-103">지원 티켓을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-103">Updates support ticket.</span></span>

## <span data-ttu-id="770b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="770b2-104">SYNTAX</span></span>

### <span data-ttu-id="770b2-105">UpdateByNameWithContactDetailParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="770b2-105">UpdateByNameWithContactDetailParameterSet (Default)</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770b2-106">UpdateByNameWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="770b2-106">UpdateByNameWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] -CustomerContactDetail <PSContactProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770b2-107">UpdateByInputObjectWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="770b2-107">UpdateByInputObjectWithContactDetailParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770b2-108">UpdateByInputObjectWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="770b2-108">UpdateByInputObjectWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>]
 -CustomerContactDetail <PSContactProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="770b2-109">설명은</span><span class="sxs-lookup"><span data-stu-id="770b2-109">DESCRIPTION</span></span>
<span data-ttu-id="770b2-110">이 cmdlet을 사용 하 여 지원 티켓의 심각도 수준, 상태 또는 고객 연락처 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-110">Use this cmdlet to update a support ticket's severity level, status or customer contact details.</span></span> <span data-ttu-id="770b2-111">지원 엔지니어에 게 티켓을 할당 하는 경우 지원 티켓의 심각도 수준을 업데이트 하거나 상태를 허용 하지 않는 것을 참고 하세요.</span><span class="sxs-lookup"><span data-stu-id="770b2-111">Note that updating a support ticket's severity level or status is not allowed when the ticket is assigned to a support engineer.</span></span> <span data-ttu-id="770b2-112">티켓을 배정한 후 심각도 수준이 나 상태를 업데이트 하려는 경우 티켓에 통신을 전송 하 여 지원 엔지니어에 게 문의 하세요.</span><span class="sxs-lookup"><span data-stu-id="770b2-112">If you wish to update the severity level or status after ticket assignment, contact the support engineer by sending a communication on the ticket.</span></span>

## <span data-ttu-id="770b2-113">예제의</span><span class="sxs-lookup"><span data-stu-id="770b2-113">EXAMPLES</span></span>

### <span data-ttu-id="770b2-114">예제 1: 지원 티켓의 심각도를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-114">Example 1: Update severity of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="770b2-115">예제 2: 지원 티켓의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-115">Example 2: Update status of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="770b2-116">예제 3: contact 개체를 지정 하 여 지원 티켓의 연락처 세부 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-116">Example 3: Update contact details of support ticket by specify contact object.</span></span>
```powershell
PS C:\> $contactDetail = new-object Microsoft.Azure.Commands.Support.Models.PSContactProfile
PS C:\> $contactDetail.FirstName = "first name updated"
PS C:\> $contactDetail.LastName = "last name updated"
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerContactDetail $contactDetail 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="770b2-117">예제 4: 파이핑 지원 티켓 개체에 따라 지원 티켓의 심각도를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-117">Example 4: Update severity of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="770b2-118">예제 5: 개별 연락처 매개 변수를 지정 하 여 지원 티켓의 연락처 세부 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-118">Example 5: Update contact details of support ticket by specifying individual contact parameters.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerFirstName "first name updated" -CustomerLastName "last name updated" -AdditionalEmailAddress @("user2@contoso.com") 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="770b2-119">예제 6: 파이핑 지원 티켓 개체에 따라 지원 티켓의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-119">Example 6: Update status of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="770b2-120">변수</span><span class="sxs-lookup"><span data-stu-id="770b2-120">PARAMETERS</span></span>

### <span data-ttu-id="770b2-121">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="770b2-121">-AdditionalEmailAddress</span></span>
<span data-ttu-id="770b2-122">추가 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-122">Additional email addresses.</span></span>
<span data-ttu-id="770b2-123">여기에 나열 된 전자 메일 주소는 지원 티켓에 대 한 모든 서신에 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-123">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="770b2-124">-Customer연락처 세부 정보</span><span class="sxs-lookup"><span data-stu-id="770b2-124">-CustomerContactDetail</span></span>
<span data-ttu-id="770b2-125">SupportTicket의 연락처 세부 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-125">Update Contact details on SupportTicket.</span></span>

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

### <span data-ttu-id="770b2-126">-고객 국가</span><span class="sxs-lookup"><span data-stu-id="770b2-126">-CustomerCountry</span></span>
<span data-ttu-id="770b2-127">고객 국가.</span><span class="sxs-lookup"><span data-stu-id="770b2-127">Customer country.</span></span>
<span data-ttu-id="770b2-128">유효한 ISO Alpha-3 국가 코드 (ISO 3166) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-128">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="770b2-129">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="770b2-129">-CustomerFirstName</span></span>
<span data-ttu-id="770b2-130">고객 성.</span><span class="sxs-lookup"><span data-stu-id="770b2-130">Customer first name.</span></span>

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

### <span data-ttu-id="770b2-131">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="770b2-131">-CustomerLastName</span></span>
<span data-ttu-id="770b2-132">고객 성.</span><span class="sxs-lookup"><span data-stu-id="770b2-132">Customer last name.</span></span>

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

### <span data-ttu-id="770b2-133">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="770b2-133">-CustomerPhoneNumber</span></span>
<span data-ttu-id="770b2-134">고객 전화 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-134">Customer phone number.</span></span>
<span data-ttu-id="770b2-135">이는 기본 연락 방법이 휴대폰 인 경우 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-135">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="770b2-136">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="770b2-136">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="770b2-137">고객 선호 지원 언어.</span><span class="sxs-lookup"><span data-stu-id="770b2-137">Customer preferred support language.</span></span>
<span data-ttu-id="770b2-138">여기에 나열 된 지원 언어 중 하나에 대 한 올바른 언어 contry 코드 여야 합니다 https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="770b2-138">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="770b2-139">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="770b2-139">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="770b2-140">고객 기본 설정 표준 시간대</span><span class="sxs-lookup"><span data-stu-id="770b2-140">Customer preferred time zone.</span></span>
<span data-ttu-id="770b2-141">유효한 System.TimeZoneInfo.Id 값 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-141">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="770b2-142">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="770b2-142">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="770b2-143">고객 기본 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-143">Customer primary email address.</span></span>

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

### <span data-ttu-id="770b2-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770b2-144">-DefaultProfile</span></span>
<span data-ttu-id="770b2-145">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="770b2-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="770b2-146">-InputObject</span></span>
<span data-ttu-id="770b2-147">이 cmdlet이 업데이트 하는 SupportTicket resource 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-147">SupportTicket resource object that this cmdlet updates.</span></span>

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

### <span data-ttu-id="770b2-148">-이름</span><span class="sxs-lookup"><span data-stu-id="770b2-148">-Name</span></span>
<span data-ttu-id="770b2-149">이 cmdlet이 업데이트 하는 SupportTicket 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-149">Name of SupportTicket resource that this cmdlet updates.</span></span>

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

### <span data-ttu-id="770b2-150">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="770b2-150">-PreferredContactMethod</span></span>
<span data-ttu-id="770b2-151">선호 연락 방법.</span><span class="sxs-lookup"><span data-stu-id="770b2-151">Preferred contact method.</span></span>

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

### <span data-ttu-id="770b2-152">-심각도</span><span class="sxs-lookup"><span data-stu-id="770b2-152">-Severity</span></span>
<span data-ttu-id="770b2-153">SupportTicket의 심각도를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-153">Update Severity of SupportTicket.</span></span>

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

### <span data-ttu-id="770b2-154">-상태</span><span class="sxs-lookup"><span data-stu-id="770b2-154">-Status</span></span>
<span data-ttu-id="770b2-155">SupportTicket의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-155">Update Status of SupportTicket.</span></span>

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

### <span data-ttu-id="770b2-156">-확인</span><span class="sxs-lookup"><span data-stu-id="770b2-156">-Confirm</span></span>
<span data-ttu-id="770b2-157">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="770b2-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="770b2-158">-WhatIf</span></span>
<span data-ttu-id="770b2-159">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="770b2-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="770b2-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770b2-161">CommonParameters</span></span>
<span data-ttu-id="770b2-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="770b2-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770b2-163">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="770b2-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770b2-164">입력</span><span class="sxs-lookup"><span data-stu-id="770b2-164">INPUTS</span></span>

### <span data-ttu-id="770b2-165">Microsoft. PSSupportTicket을 통해 지원 되는 모델</span><span class="sxs-lookup"><span data-stu-id="770b2-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="770b2-166">출력</span><span class="sxs-lookup"><span data-stu-id="770b2-166">OUTPUTS</span></span>

### <span data-ttu-id="770b2-167">Microsoft. PSSupportTicket을 통해 지원 되는 모델</span><span class="sxs-lookup"><span data-stu-id="770b2-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="770b2-168">상속자</span><span class="sxs-lookup"><span data-stu-id="770b2-168">NOTES</span></span>

## <span data-ttu-id="770b2-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="770b2-169">RELATED LINKS</span></span>
