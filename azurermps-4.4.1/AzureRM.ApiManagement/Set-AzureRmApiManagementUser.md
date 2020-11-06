---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: a9d36dca9894a10c76f2ca5a96880f4aafecb5e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525743"
---
# <span data-ttu-id="fc032-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="fc032-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="fc032-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc032-102">SYNOPSIS</span></span>
<span data-ttu-id="fc032-103">사용자 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc032-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc032-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <String>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc032-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fc032-105">DESCRIPTION</span></span>
<span data-ttu-id="fc032-106">**AzureRmApiManagementUser** cmdlet은 사용자 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="fc032-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fc032-107">EXAMPLES</span></span>

### <span data-ttu-id="fc032-108">예제 1: 사용자 암호, 전자 메일 주소 및 상태 변경</span><span class="sxs-lookup"><span data-stu-id="fc032-108">Example 1: Change a user's password, email address and state</span></span>
```
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password "asdfgh" -State "Blocked"
```

<span data-ttu-id="fc032-109">이 명령은 새 사용자 암호와 전자 메일 주소를 설정 하 고 사용자를 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="fc032-110">변수</span><span class="sxs-lookup"><span data-stu-id="fc032-110">PARAMETERS</span></span>

### <span data-ttu-id="fc032-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="fc032-111">-Context</span></span>
<span data-ttu-id="fc032-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="fc032-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-113">This parameter is required.</span></span>

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

### <span data-ttu-id="fc032-114">-전자 메일</span><span class="sxs-lookup"><span data-stu-id="fc032-114">-Email</span></span>
<span data-ttu-id="fc032-115">사용자의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-115">Specifies the email address of the user.</span></span>
<span data-ttu-id="fc032-116">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="fc032-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="fc032-117">-FirstName</span></span>
<span data-ttu-id="fc032-118">사용자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="fc032-119">이 매개 변수는 1 ~ 100 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="fc032-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="fc032-120">-LastName</span></span>
<span data-ttu-id="fc032-121">사용자의 성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="fc032-122">이 매개 변수는 1 ~ 100 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-122">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="fc032-123">-메모</span><span class="sxs-lookup"><span data-stu-id="fc032-123">-Note</span></span>
<span data-ttu-id="fc032-124">사용자에 대 한 메모를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-124">Specifies a note about the user.</span></span>
<span data-ttu-id="fc032-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-125">This parameter is optional.</span></span>
<span data-ttu-id="fc032-126">이 매개 변수의 기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-126">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="fc032-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc032-127">-PassThru</span></span>
<span data-ttu-id="fc032-128">passthru</span><span class="sxs-lookup"><span data-stu-id="fc032-128">passthru</span></span>

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

### <span data-ttu-id="fc032-129">-암호</span><span class="sxs-lookup"><span data-stu-id="fc032-129">-Password</span></span>
<span data-ttu-id="fc032-130">사용자 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-130">Specifies the user password.</span></span>
<span data-ttu-id="fc032-131">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="fc032-132">-상태</span><span class="sxs-lookup"><span data-stu-id="fc032-132">-State</span></span>
<span data-ttu-id="fc032-133">사용자 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-133">Specifies the user state.</span></span>
<span data-ttu-id="fc032-134">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-134">This parameter is optional.</span></span>
<span data-ttu-id="fc032-135">기본값은 활성입니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-135">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc032-136">-UserId</span><span class="sxs-lookup"><span data-stu-id="fc032-136">-UserId</span></span>
<span data-ttu-id="fc032-137">사용자 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-137">Specifies the user ID.</span></span>
<span data-ttu-id="fc032-138">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-138">This parameter is required.</span></span>

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

### <span data-ttu-id="fc032-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc032-139">-DefaultProfile</span></span>
<span data-ttu-id="fc032-140">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc032-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc032-141">CommonParameters</span></span>
<span data-ttu-id="fc032-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc032-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc032-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc032-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc032-144">입력</span><span class="sxs-lookup"><span data-stu-id="fc032-144">INPUTS</span></span>

## <span data-ttu-id="fc032-145">출력</span><span class="sxs-lookup"><span data-stu-id="fc032-145">OUTPUTS</span></span>

### <span data-ttu-id="fc032-146">ApiManagement. ServiceManagement. \ PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="fc032-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="fc032-147">상속자</span><span class="sxs-lookup"><span data-stu-id="fc032-147">NOTES</span></span>

## <span data-ttu-id="fc032-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc032-148">RELATED LINKS</span></span>

[<span data-ttu-id="fc032-149">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="fc032-149">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="fc032-150">새로운 AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="fc032-150">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="fc032-151">제거-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="fc032-151">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


