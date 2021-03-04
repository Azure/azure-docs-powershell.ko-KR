---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 7e141cb5c1bde59bec9e981ffd228dba6db33089
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959179"
---
# <span data-ttu-id="732a6-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="732a6-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="732a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="732a6-102">SYNOPSIS</span></span>
<span data-ttu-id="732a6-103">새 사용자를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="732a6-103">Registers a new user.</span></span>

## <span data-ttu-id="732a6-104">구문</span><span class="sxs-lookup"><span data-stu-id="732a6-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="732a6-105">설명</span><span class="sxs-lookup"><span data-stu-id="732a6-105">DESCRIPTION</span></span>
<span data-ttu-id="732a6-106">**New-AzApiManagementUser** cmdlet은 새 사용자를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="732a6-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="732a6-107">예제</span><span class="sxs-lookup"><span data-stu-id="732a6-107">EXAMPLES</span></span>

### <span data-ttu-id="732a6-108">예제 1: 새 사용자 등록</span><span class="sxs-lookup"><span data-stu-id="732a6-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="732a6-109">이 명령은 Patti Fuller라는 새 사용자를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="732a6-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="732a6-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="732a6-110">PARAMETERS</span></span>

### <span data-ttu-id="732a6-111">-Context</span><span class="sxs-lookup"><span data-stu-id="732a6-111">-Context</span></span>
<span data-ttu-id="732a6-112">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="732a6-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="732a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="732a6-113">-DefaultProfile</span></span>
<span data-ttu-id="732a6-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="732a6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="732a6-115">-email</span><span class="sxs-lookup"><span data-stu-id="732a6-115">-Email</span></span>
<span data-ttu-id="732a6-116">사용자의 전자 메일 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="732a6-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="732a6-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="732a6-117">-FirstName</span></span>
<span data-ttu-id="732a6-118">사용자의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="732a6-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="732a6-119">이 매개 변수는 1~100자입니다.</span><span class="sxs-lookup"><span data-stu-id="732a6-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="732a6-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="732a6-120">-LastName</span></span>
<span data-ttu-id="732a6-121">사용자의 성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="732a6-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="732a6-122">이 매개 변수는 1~100자입니다.</span><span class="sxs-lookup"><span data-stu-id="732a6-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="732a6-123">-Note</span><span class="sxs-lookup"><span data-stu-id="732a6-123">-Note</span></span>
<span data-ttu-id="732a6-124">사용자에 대한 메모를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="732a6-124">Specifies a note about the user.</span></span>
<span data-ttu-id="732a6-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="732a6-125">This parameter is optional.</span></span>
<span data-ttu-id="732a6-126">기본값은 $Null.</span><span class="sxs-lookup"><span data-stu-id="732a6-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="732a6-127">-Password</span><span class="sxs-lookup"><span data-stu-id="732a6-127">-Password</span></span>
<span data-ttu-id="732a6-128">사용자 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="732a6-128">Specifies the user password.</span></span>
<span data-ttu-id="732a6-129">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="732a6-129">This parameter is required.</span></span>

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

### <span data-ttu-id="732a6-130">-State</span><span class="sxs-lookup"><span data-stu-id="732a6-130">-State</span></span>
<span data-ttu-id="732a6-131">사용자 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="732a6-131">Specifies the user state.</span></span>
<span data-ttu-id="732a6-132">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="732a6-132">This parameter is optional.</span></span>
<span data-ttu-id="732a6-133">이 매개 변수의 기본값은 $Null.</span><span class="sxs-lookup"><span data-stu-id="732a6-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="732a6-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="732a6-134">-UserId</span></span>
<span data-ttu-id="732a6-135">사용자 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="732a6-135">Specifies the user ID.</span></span>
<span data-ttu-id="732a6-136">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="732a6-136">This parameter is optional.</span></span>
<span data-ttu-id="732a6-137">이 매개 변수를 지정하지 않으면 이 cmdlet에서 사용자 ID를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="732a6-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="732a6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="732a6-138">CommonParameters</span></span>
<span data-ttu-id="732a6-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="732a6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="732a6-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="732a6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="732a6-141">입력</span><span class="sxs-lookup"><span data-stu-id="732a6-141">INPUTS</span></span>

### <span data-ttu-id="732a6-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="732a6-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="732a6-143">System.String</span><span class="sxs-lookup"><span data-stu-id="732a6-143">System.String</span></span>

### <span data-ttu-id="732a6-144">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="732a6-144">System.Security.SecureString</span></span>

### <span data-ttu-id="732a6-145">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="732a6-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="732a6-146">출력</span><span class="sxs-lookup"><span data-stu-id="732a6-146">OUTPUTS</span></span>

### <span data-ttu-id="732a6-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="732a6-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="732a6-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="732a6-148">NOTES</span></span>

## <span data-ttu-id="732a6-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="732a6-149">RELATED LINKS</span></span>

[<span data-ttu-id="732a6-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="732a6-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="732a6-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="732a6-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


