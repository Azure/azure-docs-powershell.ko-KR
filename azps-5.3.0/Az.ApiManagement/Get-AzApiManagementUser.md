---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
ms.openlocfilehash: 44f351870e97d227484bd09be1e75b8cb19ac723
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494417"
---
# <span data-ttu-id="5210c-101">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5210c-101">Get-AzApiManagementUser</span></span>

## <span data-ttu-id="5210c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5210c-102">SYNOPSIS</span></span>
<span data-ttu-id="5210c-103">사용자 또는 사용자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-103">Gets a user or users.</span></span>

## <span data-ttu-id="5210c-104">구문</span><span class="sxs-lookup"><span data-stu-id="5210c-104">SYNTAX</span></span>

### <span data-ttu-id="5210c-105">GeAllUsers(기본값)</span><span class="sxs-lookup"><span data-stu-id="5210c-105">GeAllUsers (Default)</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5210c-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="5210c-106">GetByUserId</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5210c-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="5210c-107">GetByUser</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5210c-108">설명</span><span class="sxs-lookup"><span data-stu-id="5210c-108">DESCRIPTION</span></span>
<span data-ttu-id="5210c-109">**Get-AzApiManagementUser** cmdlet은 사용자가 지정되지 않은 경우 지정된 사용자 또는 모든 사용자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-109">The **Get-AzApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="5210c-110">예제</span><span class="sxs-lookup"><span data-stu-id="5210c-110">EXAMPLES</span></span>

### <span data-ttu-id="5210c-111">예제 1: 모든 사용자 얻기</span><span class="sxs-lookup"><span data-stu-id="5210c-111">Example 1: Get all users</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext
```

<span data-ttu-id="5210c-112">이 명령은 모든 사용자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-112">This command gets all users.</span></span>

### <span data-ttu-id="5210c-113">예제 2: ID로 사용자 얻기</span><span class="sxs-lookup"><span data-stu-id="5210c-113">Example 2: Get a user by ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="5210c-114">이 명령은 ID로 사용자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="5210c-115">예제 3: 성으로 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="5210c-115">Example 3: Get users by last name</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="5210c-116">이 명령은 지정된 성( Fuller)이 있는 사용자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="5210c-117">예제 4: 전자 메일 주소로 사용자 확인</span><span class="sxs-lookup"><span data-stu-id="5210c-117">Example 4: Get a user by email address</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="5210c-118">이 명령은 지정된 전자 메일 주소가 있는 사용자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="5210c-119">예제 5: 그룹 내의 모든 사용자 얻기</span><span class="sxs-lookup"><span data-stu-id="5210c-119">Example 5: Get all users within a group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="5210c-120">이 명령은 지정된 그룹 내의 모든 사용자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="5210c-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5210c-121">PARAMETERS</span></span>

### <span data-ttu-id="5210c-122">-Context</span><span class="sxs-lookup"><span data-stu-id="5210c-122">-Context</span></span>
<span data-ttu-id="5210c-123">**PsApiManagementContext의 인스턴스를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="5210c-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5210c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5210c-124">-DefaultProfile</span></span>
<span data-ttu-id="5210c-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5210c-126">-Email</span><span class="sxs-lookup"><span data-stu-id="5210c-126">-Email</span></span>
<span data-ttu-id="5210c-127">사용자의 이메일 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="5210c-128">이 매개 변수를 지정하면 이 cmdlet은 전자 메일로 사용자를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="5210c-129">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="5210c-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="5210c-130">-FirstName</span></span>
<span data-ttu-id="5210c-131">사용자의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="5210c-132">이 매개 변수를 지정하면 이 cmdlet은 이름을 사용하여 사용자를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="5210c-133">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="5210c-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="5210c-134">-GroupId</span></span>
<span data-ttu-id="5210c-135">그룹 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-135">Specifies the group identifier.</span></span>
<span data-ttu-id="5210c-136">지정된 경우 이 cmdlet은 지정된 그룹 내의 모든 사용자를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="5210c-137">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="5210c-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="5210c-138">-LastName</span></span>
<span data-ttu-id="5210c-139">사용자의 성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="5210c-140">지정된 경우 이 cmdlet은 성으로 사용자를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="5210c-141">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="5210c-142">-State</span><span class="sxs-lookup"><span data-stu-id="5210c-142">-State</span></span>
<span data-ttu-id="5210c-143">사용자 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-143">Specifies the user state.</span></span>
<span data-ttu-id="5210c-144">지정된 경우 이 cmdlet은 이 상태의 사용자를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="5210c-145">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="5210c-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="5210c-146">-UserId</span></span>
<span data-ttu-id="5210c-147">사용자 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-147">Specifies a user ID.</span></span>
<span data-ttu-id="5210c-148">지정된 경우 이 cmdlet은 이 식별자에 의해 사용자를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="5210c-149">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="5210c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5210c-150">CommonParameters</span></span>
<span data-ttu-id="5210c-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5210c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5210c-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5210c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5210c-153">입력</span><span class="sxs-lookup"><span data-stu-id="5210c-153">INPUTS</span></span>

### <span data-ttu-id="5210c-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5210c-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5210c-155">System.String</span><span class="sxs-lookup"><span data-stu-id="5210c-155">System.String</span></span>

### <span data-ttu-id="5210c-156">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="5210c-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5210c-157">출력</span><span class="sxs-lookup"><span data-stu-id="5210c-157">OUTPUTS</span></span>

### <span data-ttu-id="5210c-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5210c-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="5210c-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5210c-159">NOTES</span></span>

## <span data-ttu-id="5210c-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5210c-160">RELATED LINKS</span></span>

[<span data-ttu-id="5210c-161">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5210c-161">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="5210c-162">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5210c-162">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)

[<span data-ttu-id="5210c-163">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5210c-163">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


