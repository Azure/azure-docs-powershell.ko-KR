---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 7A45DCAD-88DC-40F0-BBF7-0F531A571CA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48b941691366c3af821e3a4cdaa7b07c5e958e16
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045445"
---
# <span data-ttu-id="30ce6-101">Select-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="30ce6-101">Select-AzureSubscription</span></span>

## <span data-ttu-id="30ce6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="30ce6-103">현재 및 기본 Azure 구독을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-103">Changes the current and default Azure subscriptions.</span></span>

## <span data-ttu-id="30ce6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30ce6-104">SYNTAX</span></span>

### <span data-ttu-id="30ce6-105">SelectSubscriptionByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="30ce6-105">SelectSubscriptionByNameParameterSet (Default)</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="30ce6-106">SelectDefaultSubscriptionByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="30ce6-106">SelectDefaultSubscriptionByNameParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="30ce6-107">SelectSubscriptionByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30ce6-107">SelectSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="30ce6-108">SelectDefaultSubscriptionByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30ce6-108">SelectDefaultSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="30ce6-109">NoCurrentSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="30ce6-109">NoCurrentSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoCurrent] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="30ce6-110">NoDefaultSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="30ce6-110">NoDefaultSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoDefault] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="30ce6-111">설명은</span><span class="sxs-lookup"><span data-stu-id="30ce6-111">DESCRIPTION</span></span>
<span data-ttu-id="30ce6-112">**AzureSubscription** cmdlet은 현재 및 기본 Azure 구독을 설정 하 고 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-112">The **Select-AzureSubscription** cmdlet sets and clears the current and default Azure subscriptions.</span></span>

<span data-ttu-id="30ce6-113">"현재 구독"은 현재 Windows PowerShell 세션에서 기본적으로 사용 되는 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-113">The "current subscription" is the subscription that is used by default in the current Windows PowerShell session.</span></span>
<span data-ttu-id="30ce6-114">"기본 구독"이 기본적으로 모든 Windows PowerShell 세션에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-114">The "default subscription" is used by default in all Windows PowerShell sessions.</span></span>
<span data-ttu-id="30ce6-115">"현재 구독" 레이블을 통해 다른 모든 세션에 대해 "기본 구독"을 변경 하지 않고 현재 세션에 대해 기본적으로 사용할 다른 구독을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-115">The "current subscription" label lets you specify a different subscription to be used by default for the current session without changing the "default subscription" for all other sessions.</span></span>

<span data-ttu-id="30ce6-116">"Default" 구독 지정이 구독 데이터 파일에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-116">The "default" subscription designation is saved in your subscription data file.</span></span>
<span data-ttu-id="30ce6-117">세션별 "현재" 지정은 저장 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-117">The session-specific "current" designation is not saved.</span></span>

<span data-ttu-id="30ce6-118">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-118">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="30ce6-119">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-119">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="30ce6-120">예제의</span><span class="sxs-lookup"><span data-stu-id="30ce6-120">EXAMPLES</span></span>

### <span data-ttu-id="30ce6-121">예제 1: 현재 구독 설정</span><span class="sxs-lookup"><span data-stu-id="30ce6-121">Example 1: Set the current subscription</span></span>
```
C:\PS> Select-AzureSubscription -Current -SubscriptionName ContosoEngineering
```

<span data-ttu-id="30ce6-122">이 명령은 현재 구독에 "ContosoEngineering"를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-122">This command makes "ContosoEngineering" the current subscription.</span></span>

### <span data-ttu-id="30ce6-123">예제 2: 기본 구독 설정</span><span class="sxs-lookup"><span data-stu-id="30ce6-123">Example 2: Set the default subscription</span></span>
```
C:\PS> Select-AzureSubscription -Default -SubscriptionName ContosoFinance -SubscriptionDataFile "C:\subs\MySubscriptions.xml"
```

<span data-ttu-id="30ce6-124">이 명령은 기본 구독을 "ContosoFinance"로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-124">This command changes the default subscription to "ContosoFinance."</span></span> <span data-ttu-id="30ce6-125">기본 구독 데이터 파일 대신 Subscriptions.xml 구독 데이터 파일에 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-125">It saves the setting in the Subscriptions.xml subscription data file, instead of the default subscription data file.</span></span>

## <span data-ttu-id="30ce6-126">변수</span><span class="sxs-lookup"><span data-stu-id="30ce6-126">PARAMETERS</span></span>

### <span data-ttu-id="30ce6-127">-계정</span><span class="sxs-lookup"><span data-stu-id="30ce6-127">-Account</span></span>
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

### <span data-ttu-id="30ce6-128">-현재</span><span class="sxs-lookup"><span data-stu-id="30ce6-128">-Current</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectSubscriptionByIdParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30ce6-129">-기본</span><span class="sxs-lookup"><span data-stu-id="30ce6-129">-Default</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectDefaultSubscriptionByNameParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30ce6-130">-NoCurrent</span><span class="sxs-lookup"><span data-stu-id="30ce6-130">-NoCurrent</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoCurrentSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30ce6-131">-NoDefault</span><span class="sxs-lookup"><span data-stu-id="30ce6-131">-NoDefault</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoDefaultSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30ce6-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30ce6-132">-PassThru</span></span>
<span data-ttu-id="30ce6-133">명령이 성공한 경우 $True를 반환 하 고 오류가 발생 하면 $False 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-133">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="30ce6-134">기본적으로이 cmdlet은 출력을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-134">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="30ce6-135">-프로필</span><span class="sxs-lookup"><span data-stu-id="30ce6-135">-Profile</span></span>
<span data-ttu-id="30ce6-136">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="30ce6-137">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="30ce6-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30ce6-138">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByIdParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30ce6-139">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="30ce6-139">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectDefaultSubscriptionByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30ce6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ce6-140">CommonParameters</span></span>
<span data-ttu-id="30ce6-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ce6-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30ce6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ce6-143">입력</span><span class="sxs-lookup"><span data-stu-id="30ce6-143">INPUTS</span></span>

### <span data-ttu-id="30ce6-144">않아야</span><span class="sxs-lookup"><span data-stu-id="30ce6-144">None</span></span>
<span data-ttu-id="30ce6-145">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="30ce6-146">출력</span><span class="sxs-lookup"><span data-stu-id="30ce6-146">OUTPUTS</span></span>

### <span data-ttu-id="30ce6-147">없음 또는 시스템 부울</span><span class="sxs-lookup"><span data-stu-id="30ce6-147">None or System.Boolean</span></span>
<span data-ttu-id="30ce6-148">*PassThru* 매개 변수를 사용 하는 경우이 Cmdlet은 부울 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="30ce6-149">기본적으로 출력은 생성 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30ce6-149">By default, it does not generate any output.</span></span>

## <span data-ttu-id="30ce6-150">상속자</span><span class="sxs-lookup"><span data-stu-id="30ce6-150">NOTES</span></span>

## <span data-ttu-id="30ce6-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30ce6-151">RELATED LINKS</span></span>

[<span data-ttu-id="30ce6-152">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="30ce6-152">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="30ce6-153">제거-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="30ce6-153">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="30ce6-154">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="30ce6-154">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


