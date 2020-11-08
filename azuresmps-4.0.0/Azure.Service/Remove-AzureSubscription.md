---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: ABC303ED-8712-4958-B871-E95357012277
online version: ''
schema: 2.0.0
ms.openlocfilehash: 706c1dee2bc4bb21a8cf116d15bfa3e53daeed99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046095"
---
# <span data-ttu-id="f0269-101">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="f0269-101">Remove-AzureSubscription</span></span>

## <span data-ttu-id="f0269-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0269-102">SYNOPSIS</span></span>
<span data-ttu-id="f0269-103">Windows PowerShell에서 Azure 구독을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-103">Deletes an Azure subscription from Windows PowerShell.</span></span>

## <span data-ttu-id="f0269-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f0269-104">SYNTAX</span></span>

### <span data-ttu-id="f0269-105">Name (기본값)</span><span class="sxs-lookup"><span data-stu-id="f0269-105">Name (Default)</span></span>
```
Remove-AzureSubscription -SubscriptionName <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0269-106">I</span><span class="sxs-lookup"><span data-stu-id="f0269-106">Id</span></span>
```
Remove-AzureSubscription -SubscriptionId <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0269-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f0269-107">DESCRIPTION</span></span>
<span data-ttu-id="f0269-108">**AzureSubscription** Cmdlet은 Windows PowerShell에서 Azure 구독을 찾을 수 없도록 구독 데이터 파일에서 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-108">The **Remove-AzureSubscription** cmdlet deletes an Azure subscription from your subscription data file so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="f0269-109">이 cmdlet은 Microsoft Azure에서 구독을 삭제 하거나 실제 구독을 어떤 방식으로든 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-109">This cmdlet does not delete the subscription from Microsoft Azure, or change the actual subscription in any way.</span></span>

<span data-ttu-id="f0269-110">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f0269-111">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="f0269-112">예제의</span><span class="sxs-lookup"><span data-stu-id="f0269-112">EXAMPLES</span></span>

### <span data-ttu-id="f0269-113">예제 1: 구독 삭제</span><span class="sxs-lookup"><span data-stu-id="f0269-113">Example 1: Delete a subscription</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test

Confirm
Are you sure you want to perform this action?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="f0269-114">이 명령은 기본 구독 데이터 파일에서 "테스트" 구독을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-114">This command deletes the "Test" subscription from the default subscription data file.</span></span>

### <span data-ttu-id="f0269-115">예제 2: 대체 구독 데이터 파일에서 삭제</span><span class="sxs-lookup"><span data-stu-id="f0269-115">Example 2: Delete from an alternate subscription data file</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test -SubscriptionDataFile C:\Subs\MySubscriptions.xml -Force
```

<span data-ttu-id="f0269-116">이 명령은 MySubscriptions.xml 구독 데이터 파일에서 테스트 구독을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-116">This command deletes the Test subscription from the MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="f0269-117">명령에서 *Force* 매개 변수를 사용 하 여 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-117">The command uses the *Force* parameter to suppress the confirmation prompt.</span></span>

### <span data-ttu-id="f0269-118">예제 3: 스크립트에서 구독 삭제</span><span class="sxs-lookup"><span data-stu-id="f0269-118">Example 3: Delete a subscription in a script</span></span>
```
C:\PS> ...if (Remove-AzureSubscription -SubscriptionName Test -PassThru) {...}
```

<span data-ttu-id="f0269-119">이 명령은 **If** 문에서 **Remove-AzureSubscription** 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-119">This command uses the **Remove-AzureSubscription** command in an **If** statement.</span></span>
<span data-ttu-id="f0269-120">이 메서드는 Boolean 값을 반환 하는 *PassThru* 매개 변수를 사용 하 여 **If** 문의 스크립트 블록이 실행 되는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-120">It uses the *PassThru* parameter, which returns a Boolean value, to determine whether the script block in the **If** statement is executed.</span></span>

## <span data-ttu-id="f0269-121">변수</span><span class="sxs-lookup"><span data-stu-id="f0269-121">PARAMETERS</span></span>

### <span data-ttu-id="f0269-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f0269-122">-Force</span></span>
<span data-ttu-id="f0269-123">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-123">Suppresses the confirmation prompt.</span></span>

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

### <span data-ttu-id="f0269-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0269-124">-PassThru</span></span>
<span data-ttu-id="f0269-125">명령이 성공한 경우 $True를 반환 하 고 오류가 발생 하면 $False 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-125">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="f0269-126">기본적으로이 cmdlet은 출력을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-126">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="f0269-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="f0269-127">-Profile</span></span>
<span data-ttu-id="f0269-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f0269-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f0269-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f0269-130">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: Id
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0269-131">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="f0269-131">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: Name
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0269-132">-확인</span><span class="sxs-lookup"><span data-stu-id="f0269-132">-Confirm</span></span>
<span data-ttu-id="f0269-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0269-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0269-134">-WhatIf</span></span>
<span data-ttu-id="f0269-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0269-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0269-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0269-137">CommonParameters</span></span>
<span data-ttu-id="f0269-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0269-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0269-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0269-140">입력</span><span class="sxs-lookup"><span data-stu-id="f0269-140">INPUTS</span></span>

### <span data-ttu-id="f0269-141">않아야</span><span class="sxs-lookup"><span data-stu-id="f0269-141">None</span></span>
<span data-ttu-id="f0269-142">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-142">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="f0269-143">출력</span><span class="sxs-lookup"><span data-stu-id="f0269-143">OUTPUTS</span></span>

### <span data-ttu-id="f0269-144">없음 또는 시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f0269-144">None or System.Boolean</span></span>
<span data-ttu-id="f0269-145">*PassThru* 매개 변수를 사용 하는 경우이 Cmdlet은 부울 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-145">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="f0269-146">그렇지 않으면 출력을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0269-146">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="f0269-147">상속자</span><span class="sxs-lookup"><span data-stu-id="f0269-147">NOTES</span></span>

## <span data-ttu-id="f0269-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0269-148">RELATED LINKS</span></span>

[<span data-ttu-id="f0269-149">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="f0269-149">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="f0269-150">선택-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="f0269-150">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)

[<span data-ttu-id="f0269-151">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="f0269-151">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


