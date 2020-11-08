---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045870"
---
# <span data-ttu-id="72259-101">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="72259-101">Remove-AzureAccount</span></span>

## <span data-ttu-id="72259-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72259-102">SYNOPSIS</span></span>
<span data-ttu-id="72259-103">Windows PowerShell에서 Azure 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="72259-103">Deletes an Azure account from Windows PowerShell.</span></span>

## <span data-ttu-id="72259-104">구문과</span><span class="sxs-lookup"><span data-stu-id="72259-104">SYNTAX</span></span>

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72259-105">설명은</span><span class="sxs-lookup"><span data-stu-id="72259-105">DESCRIPTION</span></span>
<span data-ttu-id="72259-106">**제거-AzureAccount** cmdlet은 로밍 사용자 프로필의 구독 데이터 파일에서 Azure 계정 및 해당 구독을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="72259-106">The **Remove-AzureAccount** cmdlet deletes an Azure account and its subscriptions from the subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="72259-107">Microsoft Azure에서 계정을 삭제 하거나 실제 계정이 어떤 방식으로든 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72259-107">It does not delete the account from Microsoft Azure, or change the actual account in any way.</span></span>

<span data-ttu-id="72259-108">이 cmdlet을 사용 하는 것은 Azure 계정에서 로그 아웃 하는 것과 매우 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="72259-108">Using this cmdlet is a lot like logging out of your Azure account.</span></span>
<span data-ttu-id="72259-109">계정에 다시 로그인 하려는 경우 **-azureaccount** 또는 **가져오기-Azureaccount 설정 파일** 을 사용 하 여 Windows PowerShell에 계정을 다시 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="72259-109">And, if you want to log into the account again, use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** to add the account to Windows PowerShell again.</span></span>

<span data-ttu-id="72259-110">또한 Azure PowerShell cmdlet에서 Azure 계정으로 로그인 하는 방식을 변경 하는 데 **-AzureAccount** cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72259-110">You can also use **Remove-AzureAccount** cmdlet to change the way the Azure PowerShell cmdlets sign into your Azure account.</span></span>
<span data-ttu-id="72259-111">계정에 **가져오기-Azure# settingsfile** 의 관리 인증서와 **추가-azureaccount** 의 액세스 토큰이 모두 있는 경우 Azure PowerShell cmdlet은 액세스 토큰만 사용 합니다. 관리 인증서를 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="72259-111">If your account has both a management certificate from **Import-AzurePublishSettingsFile** and an access token from **Add-AzureAccount** , the Azure PowerShell cmdlets use only the access token; they ignore the management certificate.</span></span>
<span data-ttu-id="72259-112">관리 인증서를 사용 하려면 **제거-AzureAccount** 를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="72259-112">To use the management certificate, run **Remove-AzureAccount**.</span></span>
<span data-ttu-id="72259-113">**-AzureAccount** 가 관리 인증서와 액세스 토큰을 모두 찾으면 계정을 삭제 하는 대신 액세스 토큰만 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="72259-113">When **Remove-AzureAccount** finds both a management certificate and an access token, it deletes only the access token, instead of deleting the account.</span></span>
<span data-ttu-id="72259-114">관리 인증서가 여전히 남아 있으므로 Windows PowerShell에서 계정을 계속 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72259-114">The management certificate is still there, so account is still available to Windows PowerShell.</span></span>

<span data-ttu-id="72259-115">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="72259-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="72259-116">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="72259-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="72259-117">예제의</span><span class="sxs-lookup"><span data-stu-id="72259-117">EXAMPLES</span></span>

### <span data-ttu-id="72259-118">예제 1: 계정 제거</span><span class="sxs-lookup"><span data-stu-id="72259-118">Example 1: Remove an account</span></span>
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

<span data-ttu-id="72259-119">이 명령은 admin@contoso.com 구독 데이터 파일에서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="72259-119">This command removes the admin@contoso.com from your subscription data file.</span></span>
<span data-ttu-id="72259-120">명령이 완료 되 면 Windows PowerShell에서 해당 계정을 더 이상 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="72259-120">When the command completes, the account is no longer available to Windows PowerShell.</span></span>

## <span data-ttu-id="72259-121">변수</span><span class="sxs-lookup"><span data-stu-id="72259-121">PARAMETERS</span></span>

### <span data-ttu-id="72259-122">-Force</span><span class="sxs-lookup"><span data-stu-id="72259-122">-Force</span></span>
<span data-ttu-id="72259-123">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72259-123">Suppresses the confirmation prompt.</span></span>
<span data-ttu-id="72259-124">기본적으로 **-Azureaccount 제거** 는 Windows PowerShell에서 계정을 제거 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="72259-124">By default, **Remove-AzureAccount** prompts you before removing the account from Windows PowerShell.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72259-125">-이름</span><span class="sxs-lookup"><span data-stu-id="72259-125">-Name</span></span>
<span data-ttu-id="72259-126">제거할 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72259-126">Specifies the name of the account to remove.</span></span>
<span data-ttu-id="72259-127">매개 변수 값은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="72259-127">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="72259-128">와일드 카드 문자는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72259-128">Wildcard characters are not supported.</span></span>

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

### <span data-ttu-id="72259-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72259-129">-PassThru</span></span>
<span data-ttu-id="72259-130">명령이 성공한 경우 $True를 반환 하 고 오류가 발생 하면 $False 합니다.</span><span class="sxs-lookup"><span data-stu-id="72259-130">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="72259-131">기본적으로이 cmdlet은 출력을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72259-131">By default, this cmdlet does not return any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72259-132">-프로필</span><span class="sxs-lookup"><span data-stu-id="72259-132">-Profile</span></span>
<span data-ttu-id="72259-133">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72259-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="72259-134">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="72259-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72259-135">-확인</span><span class="sxs-lookup"><span data-stu-id="72259-135">-Confirm</span></span>
<span data-ttu-id="72259-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="72259-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72259-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72259-137">-WhatIf</span></span>
<span data-ttu-id="72259-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="72259-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72259-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72259-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72259-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72259-140">CommonParameters</span></span>
<span data-ttu-id="72259-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="72259-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72259-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72259-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72259-143">입력</span><span class="sxs-lookup"><span data-stu-id="72259-143">INPUTS</span></span>

### <span data-ttu-id="72259-144">않아야</span><span class="sxs-lookup"><span data-stu-id="72259-144">None</span></span>
<span data-ttu-id="72259-145">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72259-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="72259-146">출력</span><span class="sxs-lookup"><span data-stu-id="72259-146">OUTPUTS</span></span>

### <span data-ttu-id="72259-147">없음 또는 시스템 부울</span><span class="sxs-lookup"><span data-stu-id="72259-147">None or System.Boolean</span></span>
<span data-ttu-id="72259-148">*PassThru* 매개 변수를 사용 하는 경우이 Cmdlet은 부울 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="72259-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="72259-149">그렇지 않으면 출력을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72259-149">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="72259-150">상속자</span><span class="sxs-lookup"><span data-stu-id="72259-150">NOTES</span></span>

## <span data-ttu-id="72259-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="72259-151">RELATED LINKS</span></span>

[<span data-ttu-id="72259-152">추가-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="72259-152">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="72259-153">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="72259-153">Get-AzureAccount</span></span>](./Get-AzureAccount.md)


