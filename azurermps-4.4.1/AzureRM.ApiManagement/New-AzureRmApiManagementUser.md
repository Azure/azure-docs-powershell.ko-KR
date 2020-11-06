---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: 93e6ce5a96afd1c3b297d6296c3491445593d430
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531879"
---
# <span data-ttu-id="5db2b-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5db2b-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="5db2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5db2b-102">SYNOPSIS</span></span>
<span data-ttu-id="5db2b-103">새 사용자를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5db2b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5db2b-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <String> [-State <PsApiManagementUserState>] [-Note <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5db2b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5db2b-105">DESCRIPTION</span></span>
<span data-ttu-id="5db2b-106">**새 AzureRmApiManagementUser** cmdlet은 새 사용자를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="5db2b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5db2b-107">EXAMPLES</span></span>

### <span data-ttu-id="5db2b-108">예제 1: 새 사용자 등록</span><span class="sxs-lookup"><span data-stu-id="5db2b-108">Example 1: Register a new user</span></span>
```
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password "qwerty"
```

<span data-ttu-id="5db2b-109">이 명령은 Patti 이라는 새 사용자를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="5db2b-110">변수</span><span class="sxs-lookup"><span data-stu-id="5db2b-110">PARAMETERS</span></span>

### <span data-ttu-id="5db2b-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="5db2b-111">-Context</span></span>
<span data-ttu-id="5db2b-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5db2b-113">-전자 메일</span><span class="sxs-lookup"><span data-stu-id="5db2b-113">-Email</span></span>
<span data-ttu-id="5db2b-114">사용자의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-114">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="5db2b-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="5db2b-115">-FirstName</span></span>
<span data-ttu-id="5db2b-116">사용자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-116">Specifies the first name of the user.</span></span>
<span data-ttu-id="5db2b-117">이 매개 변수는 1 ~ 100 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-117">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="5db2b-118">-LastName</span><span class="sxs-lookup"><span data-stu-id="5db2b-118">-LastName</span></span>
<span data-ttu-id="5db2b-119">사용자의 성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-119">Specifies the last name of the user.</span></span>
<span data-ttu-id="5db2b-120">이 매개 변수는 1 ~ 100 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-120">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="5db2b-121">-메모</span><span class="sxs-lookup"><span data-stu-id="5db2b-121">-Note</span></span>
<span data-ttu-id="5db2b-122">사용자에 대 한 메모를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-122">Specifies a note about the user.</span></span>
<span data-ttu-id="5db2b-123">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-123">This parameter is optional.</span></span>
<span data-ttu-id="5db2b-124">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-124">The default value is $Null.</span></span>

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

### <span data-ttu-id="5db2b-125">-암호</span><span class="sxs-lookup"><span data-stu-id="5db2b-125">-Password</span></span>
<span data-ttu-id="5db2b-126">사용자 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-126">Specifies the user password.</span></span>
<span data-ttu-id="5db2b-127">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-127">This parameter is required.</span></span>

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

### <span data-ttu-id="5db2b-128">-상태</span><span class="sxs-lookup"><span data-stu-id="5db2b-128">-State</span></span>
<span data-ttu-id="5db2b-129">사용자 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-129">Specifies the user state.</span></span>
<span data-ttu-id="5db2b-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-130">This parameter is optional.</span></span>
<span data-ttu-id="5db2b-131">이 매개 변수의 기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-131">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5db2b-132">-UserId</span><span class="sxs-lookup"><span data-stu-id="5db2b-132">-UserId</span></span>
<span data-ttu-id="5db2b-133">사용자 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-133">Specifies the user ID.</span></span>
<span data-ttu-id="5db2b-134">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-134">This parameter is optional.</span></span>
<span data-ttu-id="5db2b-135">이 매개 변수를 지정 하지 않으면이 cmdlet은 사용자 ID를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-135">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="5db2b-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db2b-136">-DefaultProfile</span></span>
<span data-ttu-id="5db2b-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5db2b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db2b-138">CommonParameters</span></span>
<span data-ttu-id="5db2b-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db2b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db2b-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5db2b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db2b-141">입력</span><span class="sxs-lookup"><span data-stu-id="5db2b-141">INPUTS</span></span>

## <span data-ttu-id="5db2b-142">출력</span><span class="sxs-lookup"><span data-stu-id="5db2b-142">OUTPUTS</span></span>

### <span data-ttu-id="5db2b-143">ApiManagement. ServiceManagement. \ PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5db2b-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="5db2b-144">상속자</span><span class="sxs-lookup"><span data-stu-id="5db2b-144">NOTES</span></span>

## <span data-ttu-id="5db2b-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5db2b-145">RELATED LINKS</span></span>

[<span data-ttu-id="5db2b-146">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5db2b-146">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="5db2b-147">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5db2b-147">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


