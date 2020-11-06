---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: d3825b4887d2361a4bb378bfddc3085773efd84b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536131"
---
# <span data-ttu-id="bb618-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bb618-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="bb618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb618-102">SYNOPSIS</span></span>
<span data-ttu-id="bb618-103">사용자 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb618-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb618-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb618-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bb618-105">DESCRIPTION</span></span>
<span data-ttu-id="bb618-106">**AzureRmApiManagementUser** cmdlet은 사용자 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="bb618-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bb618-107">EXAMPLES</span></span>

### <span data-ttu-id="bb618-108">예제 1: 사용자 암호, 전자 메일 주소 및 상태 변경</span><span class="sxs-lookup"><span data-stu-id="bb618-108">Example 1: Change a user's password, email address and state</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="bb618-109">이 명령은 새 사용자 암호와 전자 메일 주소를 설정 하 고 사용자를 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="bb618-110">변수</span><span class="sxs-lookup"><span data-stu-id="bb618-110">PARAMETERS</span></span>

### <span data-ttu-id="bb618-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="bb618-111">-Context</span></span>
<span data-ttu-id="bb618-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="bb618-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-113">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb618-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb618-114">-DefaultProfile</span></span>
<span data-ttu-id="bb618-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb618-116">-전자 메일</span><span class="sxs-lookup"><span data-stu-id="bb618-116">-Email</span></span>
<span data-ttu-id="bb618-117">사용자의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="bb618-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-118">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb618-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="bb618-119">-FirstName</span></span>
<span data-ttu-id="bb618-120">사용자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="bb618-121">이 매개 변수는 1 ~ 100 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-121">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb618-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="bb618-122">-LastName</span></span>
<span data-ttu-id="bb618-123">사용자의 성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="bb618-124">이 매개 변수는 1 ~ 100 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-124">This parameter is must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb618-125">-메모</span><span class="sxs-lookup"><span data-stu-id="bb618-125">-Note</span></span>
<span data-ttu-id="bb618-126">사용자에 대 한 메모를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-126">Specifies a note about the user.</span></span>
<span data-ttu-id="bb618-127">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-127">This parameter is optional.</span></span>
<span data-ttu-id="bb618-128">이 매개 변수의 기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-128">The default value of this parameter is $null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb618-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb618-129">-PassThru</span></span>
<span data-ttu-id="bb618-130">passthru</span><span class="sxs-lookup"><span data-stu-id="bb618-130">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb618-131">-암호</span><span class="sxs-lookup"><span data-stu-id="bb618-131">-Password</span></span>
<span data-ttu-id="bb618-132">사용자 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-132">Specifies the user password.</span></span>
<span data-ttu-id="bb618-133">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-133">This parameter is optional.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb618-134">-상태</span><span class="sxs-lookup"><span data-stu-id="bb618-134">-State</span></span>
<span data-ttu-id="bb618-135">사용자 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-135">Specifies the user state.</span></span>
<span data-ttu-id="bb618-136">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-136">This parameter is optional.</span></span>
<span data-ttu-id="bb618-137">기본값은 활성입니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-137">The default value is Active.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb618-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="bb618-138">-UserId</span></span>
<span data-ttu-id="bb618-139">사용자 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-139">Specifies the user ID.</span></span>
<span data-ttu-id="bb618-140">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-140">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb618-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb618-141">CommonParameters</span></span>
<span data-ttu-id="bb618-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb618-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb618-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb618-144">입력</span><span class="sxs-lookup"><span data-stu-id="bb618-144">INPUTS</span></span>

### <span data-ttu-id="bb618-145">않아야</span><span class="sxs-lookup"><span data-stu-id="bb618-145">None</span></span>
<span data-ttu-id="bb618-146">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb618-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb618-147">출력</span><span class="sxs-lookup"><span data-stu-id="bb618-147">OUTPUTS</span></span>

### <span data-ttu-id="bb618-148">ApiManagement. ServiceManagement. \ PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bb618-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="bb618-149">상속자</span><span class="sxs-lookup"><span data-stu-id="bb618-149">NOTES</span></span>

## <span data-ttu-id="bb618-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb618-150">RELATED LINKS</span></span>

[<span data-ttu-id="bb618-151">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bb618-151">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="bb618-152">새로운 AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bb618-152">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="bb618-153">제거-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bb618-153">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


