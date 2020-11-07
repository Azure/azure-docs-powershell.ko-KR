---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 30ff5f7d9ead2226c6c03b4707af9c20ff40d405
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869477"
---
# <span data-ttu-id="03bfd-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="03bfd-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="03bfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03bfd-102">SYNOPSIS</span></span>
<span data-ttu-id="03bfd-103">새 사용자를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-103">Registers a new user.</span></span>

## <span data-ttu-id="03bfd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="03bfd-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03bfd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="03bfd-105">DESCRIPTION</span></span>
<span data-ttu-id="03bfd-106">**새 AzApiManagementUser** cmdlet은 새 사용자를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="03bfd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="03bfd-107">EXAMPLES</span></span>

### <span data-ttu-id="03bfd-108">예제 1: 새 사용자 등록</span><span class="sxs-lookup"><span data-stu-id="03bfd-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="03bfd-109">이 명령은 Patti 이라는 새 사용자를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="03bfd-110">변수</span><span class="sxs-lookup"><span data-stu-id="03bfd-110">PARAMETERS</span></span>

### <span data-ttu-id="03bfd-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="03bfd-111">-Context</span></span>
<span data-ttu-id="03bfd-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="03bfd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03bfd-113">-DefaultProfile</span></span>
<span data-ttu-id="03bfd-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03bfd-115">-전자 메일</span><span class="sxs-lookup"><span data-stu-id="03bfd-115">-Email</span></span>
<span data-ttu-id="03bfd-116">사용자의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="03bfd-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="03bfd-117">-FirstName</span></span>
<span data-ttu-id="03bfd-118">사용자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="03bfd-119">이 매개 변수는 1 ~ 100 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="03bfd-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="03bfd-120">-LastName</span></span>
<span data-ttu-id="03bfd-121">사용자의 성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="03bfd-122">이 매개 변수는 1 ~ 100 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="03bfd-123">-메모</span><span class="sxs-lookup"><span data-stu-id="03bfd-123">-Note</span></span>
<span data-ttu-id="03bfd-124">사용자에 대 한 메모를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-124">Specifies a note about the user.</span></span>
<span data-ttu-id="03bfd-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-125">This parameter is optional.</span></span>
<span data-ttu-id="03bfd-126">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="03bfd-127">-암호</span><span class="sxs-lookup"><span data-stu-id="03bfd-127">-Password</span></span>
<span data-ttu-id="03bfd-128">사용자 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-128">Specifies the user password.</span></span>
<span data-ttu-id="03bfd-129">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-129">This parameter is required.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03bfd-130">-상태</span><span class="sxs-lookup"><span data-stu-id="03bfd-130">-State</span></span>
<span data-ttu-id="03bfd-131">사용자 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-131">Specifies the user state.</span></span>
<span data-ttu-id="03bfd-132">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-132">This parameter is optional.</span></span>
<span data-ttu-id="03bfd-133">이 매개 변수의 기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03bfd-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="03bfd-134">-UserId</span></span>
<span data-ttu-id="03bfd-135">사용자 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-135">Specifies the user ID.</span></span>
<span data-ttu-id="03bfd-136">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-136">This parameter is optional.</span></span>
<span data-ttu-id="03bfd-137">이 매개 변수를 지정 하지 않으면이 cmdlet은 사용자 ID를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="03bfd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03bfd-138">CommonParameters</span></span>
<span data-ttu-id="03bfd-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bfd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03bfd-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03bfd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03bfd-141">입력</span><span class="sxs-lookup"><span data-stu-id="03bfd-141">INPUTS</span></span>

### <span data-ttu-id="03bfd-142">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="03bfd-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="03bfd-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="03bfd-143">System.String</span></span>

### <span data-ttu-id="03bfd-144">System.webserver</span><span class="sxs-lookup"><span data-stu-id="03bfd-144">System.Security.SecureString</span></span>

### <span data-ttu-id="03bfd-145">시스템 Null 허용 ' 1 [[ApiManagement]. ServiceManagement, PsApiManagementUserState, Microsoft azure. PowerShell. ApiManagement, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="03bfd-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="03bfd-146">출력</span><span class="sxs-lookup"><span data-stu-id="03bfd-146">OUTPUTS</span></span>

### <span data-ttu-id="03bfd-147">ApiManagement. ServiceManagement. \ PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="03bfd-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="03bfd-148">상속자</span><span class="sxs-lookup"><span data-stu-id="03bfd-148">NOTES</span></span>

## <span data-ttu-id="03bfd-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03bfd-149">RELATED LINKS</span></span>

[<span data-ttu-id="03bfd-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="03bfd-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="03bfd-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="03bfd-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


