---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: be6c9ee6c0db12e324786052348209703b79601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525796"
---
# <span data-ttu-id="a14f7-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a14f7-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="a14f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a14f7-102">SYNOPSIS</span></span>
<span data-ttu-id="a14f7-103">한 명 이상의 사용자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a14f7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a14f7-104">SYNTAX</span></span>

### <span data-ttu-id="a14f7-105">모든 사용자 가져오기 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a14f7-105">Get all users (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a14f7-106">ID를 사용 하 여 사용자 가져오기</span><span class="sxs-lookup"><span data-stu-id="a14f7-106">Get user by ID</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a14f7-107">사용자 찾기</span><span class="sxs-lookup"><span data-stu-id="a14f7-107">Find users</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a14f7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a14f7-108">DESCRIPTION</span></span>
<span data-ttu-id="a14f7-109">**AzureRmApiManagementUser** cmdlet은 지정 된 사용자를 지정 하지 않으면 모든 사용자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="a14f7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a14f7-110">EXAMPLES</span></span>

### <span data-ttu-id="a14f7-111">예제 1: 모든 사용자 가져오기</span><span class="sxs-lookup"><span data-stu-id="a14f7-111">Example 1: Get all users</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="a14f7-112">이 명령은 모든 사용자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-112">This command gets all users.</span></span>

### <span data-ttu-id="a14f7-113">예제 2: ID를 사용 하 여 사용자 가져오기</span><span class="sxs-lookup"><span data-stu-id="a14f7-113">Example 2: Get a user by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="a14f7-114">이 명령은 ID를 사용 하 여 사용자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="a14f7-115">예: 성을 기준으로 사용자 가져오기</span><span class="sxs-lookup"><span data-stu-id="a14f7-115">Example: Get users by last name</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="a14f7-116">이 명령은 지정 된 성, 보다 자세한 이름을 가진 사용자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="a14f7-117">예제 4: 전자 메일 주소로 사용자 가져오기</span><span class="sxs-lookup"><span data-stu-id="a14f7-117">Example 4: Get a user by email address</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email 
"user@contoso.com"
```

<span data-ttu-id="a14f7-118">이 명령은 지정 된 전자 메일 주소를 가진 사용자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="a14f7-119">예제 5: 그룹 내의 모든 사용자 가져오기</span><span class="sxs-lookup"><span data-stu-id="a14f7-119">Example 5: Get all users within a group</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="a14f7-120">이 명령은 지정 된 그룹 내의 모든 사용자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="a14f7-121">변수</span><span class="sxs-lookup"><span data-stu-id="a14f7-121">PARAMETERS</span></span>

### <span data-ttu-id="a14f7-122">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="a14f7-122">-Context</span></span>
<span data-ttu-id="a14f7-123">**PsApiManagementContext** 의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-123">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="a14f7-124">-전자 메일</span><span class="sxs-lookup"><span data-stu-id="a14f7-124">-Email</span></span>
<span data-ttu-id="a14f7-125">사용자의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-125">Specifies the email address of the user.</span></span>
<span data-ttu-id="a14f7-126">이 매개 변수를 지정 하면이 cmdlet이 사용자를 전자 메일로 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-126">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="a14f7-127">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-127">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a14f7-128">-FirstName</span><span class="sxs-lookup"><span data-stu-id="a14f7-128">-FirstName</span></span>
<span data-ttu-id="a14f7-129">사용자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-129">Specifies the first name of the user.</span></span>
<span data-ttu-id="a14f7-130">이 매개 변수를 지정 하면이 cmdlet은 이름으로 사용자를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-130">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="a14f7-131">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-131">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a14f7-132">-GroupId</span><span class="sxs-lookup"><span data-stu-id="a14f7-132">-GroupId</span></span>
<span data-ttu-id="a14f7-133">그룹 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-133">Specifies the group identifier.</span></span>
<span data-ttu-id="a14f7-134">지정 된 경우이 cmdlet은 지정 된 그룹 내의 모든 사용자를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-134">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="a14f7-135">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-135">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a14f7-136">-LastName</span><span class="sxs-lookup"><span data-stu-id="a14f7-136">-LastName</span></span>
<span data-ttu-id="a14f7-137">사용자의 성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-137">Specifies the last name of a user.</span></span>
<span data-ttu-id="a14f7-138">지정 된 경우이 cmdlet은 성을 기준으로 사용자를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-138">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="a14f7-139">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-139">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a14f7-140">-상태</span><span class="sxs-lookup"><span data-stu-id="a14f7-140">-State</span></span>
<span data-ttu-id="a14f7-141">사용자 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-141">Specifies the user state.</span></span>
<span data-ttu-id="a14f7-142">지정 된 경우이 cmdlet은이 상태의 사용자를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-142">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="a14f7-143">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-143">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: Find users
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a14f7-144">-UserId</span><span class="sxs-lookup"><span data-stu-id="a14f7-144">-UserId</span></span>
<span data-ttu-id="a14f7-145">사용자 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-145">Specifies a user ID.</span></span>
<span data-ttu-id="a14f7-146">지정 된 경우이 cmdlet은이 식별자를 사용 하 여 사용자를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-146">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="a14f7-147">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-147">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Get user by ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a14f7-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a14f7-148">-DefaultProfile</span></span>
<span data-ttu-id="a14f7-149">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a14f7-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a14f7-150">CommonParameters</span></span>
<span data-ttu-id="a14f7-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a14f7-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a14f7-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a14f7-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a14f7-153">입력</span><span class="sxs-lookup"><span data-stu-id="a14f7-153">INPUTS</span></span>

## <span data-ttu-id="a14f7-154">출력</span><span class="sxs-lookup"><span data-stu-id="a14f7-154">OUTPUTS</span></span>

### <span data-ttu-id="a14f7-155">IList를<ApiManagement> ServiceManagement. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a14f7-155">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser></span></span>

## <span data-ttu-id="a14f7-156">상속자</span><span class="sxs-lookup"><span data-stu-id="a14f7-156">NOTES</span></span>

## <span data-ttu-id="a14f7-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a14f7-157">RELATED LINKS</span></span>

[<span data-ttu-id="a14f7-158">새로운 AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a14f7-158">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="a14f7-159">제거-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a14f7-159">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="a14f7-160">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a14f7-160">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


