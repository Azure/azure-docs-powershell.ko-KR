---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
ms.openlocfilehash: 1734eeb341d850f61fa3d5e930cabc26a4060de6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689123"
---
# <span data-ttu-id="22262-101">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="22262-101">Get-AzApiManagementUser</span></span>

## <span data-ttu-id="22262-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22262-102">SYNOPSIS</span></span>
<span data-ttu-id="22262-103">한 명 이상의 사용자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22262-103">Gets a user or users.</span></span>

## <span data-ttu-id="22262-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22262-104">SYNTAX</span></span>

### <span data-ttu-id="22262-105">GeAllUsers (기본값)</span><span class="sxs-lookup"><span data-stu-id="22262-105">GeAllUsers (Default)</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22262-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="22262-106">GetByUserId</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22262-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="22262-107">GetByUser</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22262-108">설명은</span><span class="sxs-lookup"><span data-stu-id="22262-108">DESCRIPTION</span></span>
<span data-ttu-id="22262-109">**AzApiManagementUser** cmdlet은 지정 된 사용자를 지정 하지 않으면 모든 사용자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22262-109">The **Get-AzApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="22262-110">예제의</span><span class="sxs-lookup"><span data-stu-id="22262-110">EXAMPLES</span></span>

### <span data-ttu-id="22262-111">예제 1: 모든 사용자 가져오기</span><span class="sxs-lookup"><span data-stu-id="22262-111">Example 1: Get all users</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext
```

<span data-ttu-id="22262-112">이 명령은 모든 사용자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22262-112">This command gets all users.</span></span>

### <span data-ttu-id="22262-113">예제 2: ID를 사용 하 여 사용자 가져오기</span><span class="sxs-lookup"><span data-stu-id="22262-113">Example 2: Get a user by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="22262-114">이 명령은 ID를 사용 하 여 사용자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22262-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="22262-115">예: 성을 기준으로 사용자 가져오기</span><span class="sxs-lookup"><span data-stu-id="22262-115">Example: Get users by last name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="22262-116">이 명령은 지정 된 성, 보다 자세한 이름을 가진 사용자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22262-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="22262-117">예제 4: 전자 메일 주소로 사용자 가져오기</span><span class="sxs-lookup"><span data-stu-id="22262-117">Example 4: Get a user by email address</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="22262-118">이 명령은 지정 된 전자 메일 주소를 가진 사용자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22262-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="22262-119">예제 5: 그룹 내의 모든 사용자 가져오기</span><span class="sxs-lookup"><span data-stu-id="22262-119">Example 5: Get all users within a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="22262-120">이 명령은 지정 된 그룹 내의 모든 사용자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22262-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="22262-121">변수</span><span class="sxs-lookup"><span data-stu-id="22262-121">PARAMETERS</span></span>

### <span data-ttu-id="22262-122">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="22262-122">-Context</span></span>
<span data-ttu-id="22262-123">**PsApiManagementContext** 의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22262-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22262-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22262-124">-DefaultProfile</span></span>
<span data-ttu-id="22262-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="22262-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22262-126">-전자 메일</span><span class="sxs-lookup"><span data-stu-id="22262-126">-Email</span></span>
<span data-ttu-id="22262-127">사용자의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22262-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="22262-128">이 매개 변수를 지정 하면이 cmdlet이 사용자를 전자 메일로 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="22262-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="22262-129">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="22262-129">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22262-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="22262-130">-FirstName</span></span>
<span data-ttu-id="22262-131">사용자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22262-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="22262-132">이 매개 변수를 지정 하면이 cmdlet은 이름으로 사용자를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="22262-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="22262-133">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="22262-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22262-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="22262-134">-GroupId</span></span>
<span data-ttu-id="22262-135">그룹 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22262-135">Specifies the group identifier.</span></span>
<span data-ttu-id="22262-136">지정 된 경우이 cmdlet은 지정 된 그룹 내의 모든 사용자를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="22262-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="22262-137">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="22262-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22262-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="22262-138">-LastName</span></span>
<span data-ttu-id="22262-139">사용자의 성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22262-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="22262-140">지정 된 경우이 cmdlet은 성을 기준으로 사용자를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="22262-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="22262-141">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="22262-141">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22262-142">-상태</span><span class="sxs-lookup"><span data-stu-id="22262-142">-State</span></span>
<span data-ttu-id="22262-143">사용자 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22262-143">Specifies the user state.</span></span>
<span data-ttu-id="22262-144">지정 된 경우이 cmdlet은이 상태의 사용자를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="22262-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="22262-145">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="22262-145">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: GetByUser
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22262-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="22262-146">-UserId</span></span>
<span data-ttu-id="22262-147">사용자 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22262-147">Specifies a user ID.</span></span>
<span data-ttu-id="22262-148">지정 된 경우이 cmdlet은이 식별자를 사용 하 여 사용자를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="22262-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="22262-149">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="22262-149">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22262-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22262-150">CommonParameters</span></span>
<span data-ttu-id="22262-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22262-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22262-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22262-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22262-153">입력</span><span class="sxs-lookup"><span data-stu-id="22262-153">INPUTS</span></span>

### <span data-ttu-id="22262-154">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="22262-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="22262-155">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="22262-155">System.String</span></span>

### <span data-ttu-id="22262-156">시스템 Null 허용 ' 1 [[ApiManagement]. ServiceManagement, PsApiManagementUserState, Microsoft azure. PowerShell. ApiManagement, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22262-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="22262-157">출력</span><span class="sxs-lookup"><span data-stu-id="22262-157">OUTPUTS</span></span>

### <span data-ttu-id="22262-158">ApiManagement. ServiceManagement. \ PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="22262-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="22262-159">상속자</span><span class="sxs-lookup"><span data-stu-id="22262-159">NOTES</span></span>

## <span data-ttu-id="22262-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22262-160">RELATED LINKS</span></span>

[<span data-ttu-id="22262-161">새로운 AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="22262-161">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="22262-162">제거-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="22262-162">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)

[<span data-ttu-id="22262-163">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="22262-163">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


