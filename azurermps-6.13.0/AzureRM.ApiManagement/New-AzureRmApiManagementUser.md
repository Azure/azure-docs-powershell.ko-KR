---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: 1c8b7f8069c63d18f69285f7e40ac4d652f0bf73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702497"
---
# <span data-ttu-id="d51a7-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d51a7-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="d51a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d51a7-102">SYNOPSIS</span></span>
<span data-ttu-id="d51a7-103">새 사용자를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d51a7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d51a7-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d51a7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d51a7-105">DESCRIPTION</span></span>
<span data-ttu-id="d51a7-106">**새 AzureRmApiManagementUser** cmdlet은 새 사용자를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="d51a7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d51a7-107">EXAMPLES</span></span>

### <span data-ttu-id="d51a7-108">예제 1: 새 사용자 등록</span><span class="sxs-lookup"><span data-stu-id="d51a7-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="d51a7-109">이 명령은 Patti 이라는 새 사용자를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="d51a7-110">변수</span><span class="sxs-lookup"><span data-stu-id="d51a7-110">PARAMETERS</span></span>

### <span data-ttu-id="d51a7-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d51a7-111">-Context</span></span>
<span data-ttu-id="d51a7-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d51a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d51a7-113">-DefaultProfile</span></span>
<span data-ttu-id="d51a7-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d51a7-115">-전자 메일</span><span class="sxs-lookup"><span data-stu-id="d51a7-115">-Email</span></span>
<span data-ttu-id="d51a7-116">사용자의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="d51a7-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="d51a7-117">-FirstName</span></span>
<span data-ttu-id="d51a7-118">사용자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="d51a7-119">이 매개 변수는 1 ~ 100 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="d51a7-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="d51a7-120">-LastName</span></span>
<span data-ttu-id="d51a7-121">사용자의 성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="d51a7-122">이 매개 변수는 1 ~ 100 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="d51a7-123">-메모</span><span class="sxs-lookup"><span data-stu-id="d51a7-123">-Note</span></span>
<span data-ttu-id="d51a7-124">사용자에 대 한 메모를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-124">Specifies a note about the user.</span></span>
<span data-ttu-id="d51a7-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-125">This parameter is optional.</span></span>
<span data-ttu-id="d51a7-126">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="d51a7-127">-암호</span><span class="sxs-lookup"><span data-stu-id="d51a7-127">-Password</span></span>
<span data-ttu-id="d51a7-128">사용자 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-128">Specifies the user password.</span></span>
<span data-ttu-id="d51a7-129">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-129">This parameter is required.</span></span>

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

### <span data-ttu-id="d51a7-130">-상태</span><span class="sxs-lookup"><span data-stu-id="d51a7-130">-State</span></span>
<span data-ttu-id="d51a7-131">사용자 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-131">Specifies the user state.</span></span>
<span data-ttu-id="d51a7-132">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-132">This parameter is optional.</span></span>
<span data-ttu-id="d51a7-133">이 매개 변수의 기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="d51a7-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="d51a7-134">-UserId</span></span>
<span data-ttu-id="d51a7-135">사용자 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-135">Specifies the user ID.</span></span>
<span data-ttu-id="d51a7-136">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-136">This parameter is optional.</span></span>
<span data-ttu-id="d51a7-137">이 매개 변수를 지정 하지 않으면이 cmdlet은 사용자 ID를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="d51a7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d51a7-138">CommonParameters</span></span>
<span data-ttu-id="d51a7-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51a7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d51a7-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d51a7-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d51a7-141">입력</span><span class="sxs-lookup"><span data-stu-id="d51a7-141">INPUTS</span></span>

### <span data-ttu-id="d51a7-142">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d51a7-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d51a7-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d51a7-143">System.String</span></span>

### <span data-ttu-id="d51a7-144">System.webserver</span><span class="sxs-lookup"><span data-stu-id="d51a7-144">System.Security.SecureString</span></span>

### <span data-ttu-id="d51a7-145">시스템 Null 허용 ' 1 [[ApiManagement, ServiceManagement. PsApiManagementUserState, Microsoft Azure. ServiceManagement, Version = 6.1.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d51a7-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d51a7-146">출력</span><span class="sxs-lookup"><span data-stu-id="d51a7-146">OUTPUTS</span></span>

### <span data-ttu-id="d51a7-147">ApiManagement. ServiceManagement. \ PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d51a7-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="d51a7-148">상속자</span><span class="sxs-lookup"><span data-stu-id="d51a7-148">NOTES</span></span>

## <span data-ttu-id="d51a7-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d51a7-149">RELATED LINKS</span></span>

[<span data-ttu-id="d51a7-150">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d51a7-150">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="d51a7-151">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d51a7-151">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


