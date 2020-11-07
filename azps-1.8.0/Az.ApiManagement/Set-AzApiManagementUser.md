---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
ms.openlocfilehash: 03ea39c24166b6e44c057907fbc7346996d3dfa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869309"
---
# <span data-ttu-id="20bae-101">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="20bae-101">Set-AzApiManagementUser</span></span>

## <span data-ttu-id="20bae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20bae-102">SYNOPSIS</span></span>
<span data-ttu-id="20bae-103">사용자 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-103">Sets user details.</span></span>

## <span data-ttu-id="20bae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20bae-104">SYNTAX</span></span>

```
Set-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20bae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="20bae-105">DESCRIPTION</span></span>
<span data-ttu-id="20bae-106">**AzApiManagementUser** cmdlet은 사용자 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-106">The **Set-AzApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="20bae-107">예제의</span><span class="sxs-lookup"><span data-stu-id="20bae-107">EXAMPLES</span></span>

### <span data-ttu-id="20bae-108">예제 1: 사용자 암호, 전자 메일 주소 및 상태 변경</span><span class="sxs-lookup"><span data-stu-id="20bae-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="20bae-109">이 명령은 새 사용자 암호와 전자 메일 주소를 설정 하 고 사용자를 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="20bae-110">변수</span><span class="sxs-lookup"><span data-stu-id="20bae-110">PARAMETERS</span></span>

### <span data-ttu-id="20bae-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="20bae-111">-Context</span></span>
<span data-ttu-id="20bae-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="20bae-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-113">This parameter is required.</span></span>

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

### <span data-ttu-id="20bae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20bae-114">-DefaultProfile</span></span>
<span data-ttu-id="20bae-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20bae-116">-전자 메일</span><span class="sxs-lookup"><span data-stu-id="20bae-116">-Email</span></span>
<span data-ttu-id="20bae-117">사용자의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="20bae-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="20bae-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="20bae-119">-FirstName</span></span>
<span data-ttu-id="20bae-120">사용자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="20bae-121">이 매개 변수는 1 ~ 100 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="20bae-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="20bae-122">-LastName</span></span>
<span data-ttu-id="20bae-123">사용자의 성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="20bae-124">이 매개 변수는 1 ~ 100 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="20bae-125">-메모</span><span class="sxs-lookup"><span data-stu-id="20bae-125">-Note</span></span>
<span data-ttu-id="20bae-126">사용자에 대 한 메모를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-126">Specifies a note about the user.</span></span>
<span data-ttu-id="20bae-127">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-127">This parameter is optional.</span></span>
<span data-ttu-id="20bae-128">이 매개 변수의 기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="20bae-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20bae-129">-PassThru</span></span>
<span data-ttu-id="20bae-130">passthru</span><span class="sxs-lookup"><span data-stu-id="20bae-130">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20bae-131">-암호</span><span class="sxs-lookup"><span data-stu-id="20bae-131">-Password</span></span>
<span data-ttu-id="20bae-132">사용자 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-132">Specifies the user password.</span></span>
<span data-ttu-id="20bae-133">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-133">This parameter is optional.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20bae-134">-상태</span><span class="sxs-lookup"><span data-stu-id="20bae-134">-State</span></span>
<span data-ttu-id="20bae-135">사용자 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-135">Specifies the user state.</span></span>
<span data-ttu-id="20bae-136">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-136">This parameter is optional.</span></span>
<span data-ttu-id="20bae-137">기본값은 활성입니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-137">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20bae-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="20bae-138">-UserId</span></span>
<span data-ttu-id="20bae-139">사용자 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-139">Specifies the user ID.</span></span>
<span data-ttu-id="20bae-140">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-140">This parameter is required.</span></span>

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

### <span data-ttu-id="20bae-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20bae-141">CommonParameters</span></span>
<span data-ttu-id="20bae-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20bae-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20bae-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20bae-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20bae-144">입력</span><span class="sxs-lookup"><span data-stu-id="20bae-144">INPUTS</span></span>

### <span data-ttu-id="20bae-145">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="20bae-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="20bae-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="20bae-146">System.String</span></span>

### <span data-ttu-id="20bae-147">System.webserver</span><span class="sxs-lookup"><span data-stu-id="20bae-147">System.Security.SecureString</span></span>

### <span data-ttu-id="20bae-148">ApiManagement. ServiceManagement. \ PsApiManagementUserState</span><span class="sxs-lookup"><span data-stu-id="20bae-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="20bae-149">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="20bae-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="20bae-150">출력</span><span class="sxs-lookup"><span data-stu-id="20bae-150">OUTPUTS</span></span>

### <span data-ttu-id="20bae-151">ApiManagement. ServiceManagement. \ PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="20bae-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="20bae-152">상속자</span><span class="sxs-lookup"><span data-stu-id="20bae-152">NOTES</span></span>

## <span data-ttu-id="20bae-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20bae-153">RELATED LINKS</span></span>

[<span data-ttu-id="20bae-154">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="20bae-154">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="20bae-155">새로운 AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="20bae-155">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="20bae-156">제거-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="20bae-156">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)


