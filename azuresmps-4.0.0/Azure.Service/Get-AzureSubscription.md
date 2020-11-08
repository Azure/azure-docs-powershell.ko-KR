---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045537"
---
# <span data-ttu-id="7c32a-101">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="7c32a-101">Get-AzureSubscription</span></span>

## <span data-ttu-id="7c32a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c32a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c32a-103">Azure 계정에서 Azure 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-103">Gets  Azure subscriptions in Azure account.</span></span>

## <span data-ttu-id="7c32a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c32a-104">SYNTAX</span></span>

### <span data-ttu-id="7c32a-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="7c32a-105">ByName (Default)</span></span>
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c32a-106">ById</span><span class="sxs-lookup"><span data-stu-id="7c32a-106">ById</span></span>
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c32a-107">기본값</span><span class="sxs-lookup"><span data-stu-id="7c32a-107">Default</span></span>
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7c32a-108">전류</span><span class="sxs-lookup"><span data-stu-id="7c32a-108">Current</span></span>
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7c32a-109">설명은</span><span class="sxs-lookup"><span data-stu-id="7c32a-109">DESCRIPTION</span></span>
<span data-ttu-id="7c32a-110">**AzureSubscription** Cmdlet은 Azure 계정에서 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-110">The **Get-AzureSubscription** cmdlet gets the subscriptions in your Azure account.</span></span>
<span data-ttu-id="7c32a-111">이 cmdlet을 사용 하 여 구독에 대 한 정보를 가져오고 구독을 다른 cmdlet에 파이프 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-111">You can use this cmdlet to get information about the subscription and to pipe the subscription to other cmdlets.</span></span>

<span data-ttu-id="7c32a-112">**Get-AzureSubscription** 에는 Azure 계정에 대 한 액세스가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-112">**Get-AzureSubscription** requires access to your Azure accounts.</span></span>
<span data-ttu-id="7c32a-113">**AzureSubscription** 를 실행 하기 전에 게시 설정 파일을 다운로드 하 고 설치 하는 Cmdlet 또는 **추가-azureaccount** **cmdlet을 실행 해야 합니다 (가져오기** - **azureaccount settingsfile** ).</span><span class="sxs-lookup"><span data-stu-id="7c32a-113">Before you run **Get-AzureSubscription** , you must run the **Add-AzureAccount** cmdlet or the cmdlets that download and install a publish settings file ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.</span></span>

<span data-ttu-id="7c32a-114">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-114">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7c32a-115">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-115">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="7c32a-116">예제의</span><span class="sxs-lookup"><span data-stu-id="7c32a-116">EXAMPLES</span></span>

### <span data-ttu-id="7c32a-117">예제 1: 모든 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="7c32a-117">Example 1: Get all subscriptions</span></span>
```
C:\PS>Get-AzureSubscription
```

<span data-ttu-id="7c32a-118">이 명령은 계정에 있는 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-118">This command gets all subscriptions in the account.</span></span>

### <span data-ttu-id="7c32a-119">예제 2: 이름으로 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="7c32a-119">Example 2: Get a subscription by name</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

<span data-ttu-id="7c32a-120">이 명령은 "MyProdSubsciption" 구독만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-120">This command gets only the "MyProdSubsciption" subscription.</span></span>

### <span data-ttu-id="7c32a-121">예제 3: 기본 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="7c32a-121">Example 3: Get the default subscription</span></span>
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

<span data-ttu-id="7c32a-122">이 명령은 기본 구독의 이름만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-122">This command gets only the name of the default subscription.</span></span>
<span data-ttu-id="7c32a-123">이 명령은 먼저 구독을 가져온 다음 도트 메서드를 사용 하 여 구독의 **SubscriptionName** 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-123">The command first gets the subscription and then uses the dot method to get the **SubscriptionName** property of the subscription.</span></span>

### <span data-ttu-id="7c32a-124">예제 4: 선택한 구독 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="7c32a-124">Example 4: Get selected subscription properties</span></span>
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

<span data-ttu-id="7c32a-125">이 명령은 현재 구독의 이름 및 인증서를 포함 하는 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-125">This command returns a list with the name and certificate of the current subscription.</span></span>
<span data-ttu-id="7c32a-126">**Get-AzureSubscription** 명령을 사용 하 여 현재 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-126">It uses a **Get-AzureSubscription** command to get the current subscription.</span></span>
<span data-ttu-id="7c32a-127">그런 다음 구독을 목록에서 선택 된 속성을 표시 하는 **형식 목록** 명령으로 파이프 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-127">Then it pipes the subscription to a **Format-List** command that displays the selected properties in a list.</span></span>

### <span data-ttu-id="7c32a-128">예제 5: 대체 구독 데이터 파일 사용</span><span class="sxs-lookup"><span data-stu-id="7c32a-128">Example 5: Use an alternate subscription data file</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

<span data-ttu-id="7c32a-129">이 명령은 C:\Temp\MySubscriptions.xml 구독 데이터 파일에서 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-129">This command gets subscriptions from  the C:\Temp\MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="7c32a-130">**추가-AzureAccount** 또는 **가져오기-게시 파일** cmdlet을 실행할 때 대체 구독 데이터 파일을 지정한 경우에는 **subscriptiondatafile** 정보 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-130">Use the **SubscriptionDataFile** parameter if you specified an alternate subscription data file when you ran the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="7c32a-131">변수</span><span class="sxs-lookup"><span data-stu-id="7c32a-131">PARAMETERS</span></span>

### <span data-ttu-id="7c32a-132">-현재</span><span class="sxs-lookup"><span data-stu-id="7c32a-132">-Current</span></span>
<span data-ttu-id="7c32a-133">현재 구독, 즉 "current"로 지정 된 구독만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-133">Gets only the current subscription, that is, the subscription designated as "current."</span></span> <span data-ttu-id="7c32a-134">기본적으로 **Get-AzureSubscription** 는 Azure 계정의 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-134">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="7c32a-135">구독을 "current"로 지정 하려면 **AzureSubscription** Cmdlet의 **현재** 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-135">To designate a subscription as "current," use the **Current** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c32a-136">-기본</span><span class="sxs-lookup"><span data-stu-id="7c32a-136">-Default</span></span>
<span data-ttu-id="7c32a-137">기본 구독, 즉 "default"로 지정 된 구독만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-137">Gets only the default subscription, that is, the subscription designated as "default."</span></span> <span data-ttu-id="7c32a-138">기본적으로 **Get-AzureSubscription** 는 Azure 계정의 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-138">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="7c32a-139">구독을 "default"로 지정 하려면 **AzureSubscription** Cmdlet의 **기본** 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-139">To designate a subscription as "default," use the **Default** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c32a-140">-ExtendedDetails</span><span class="sxs-lookup"><span data-stu-id="7c32a-140">-ExtendedDetails</span></span>
<span data-ttu-id="7c32a-141">표준 설정 외에도 구독에 대 한 할당량 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-141">Returns quota information for the subscription, in addition to the standard settings.</span></span>

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

### <span data-ttu-id="7c32a-142">-프로필</span><span class="sxs-lookup"><span data-stu-id="7c32a-142">-Profile</span></span>
<span data-ttu-id="7c32a-143">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-143">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7c32a-144">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7c32a-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c32a-145">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c32a-146">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="7c32a-146">-SubscriptionName</span></span>
<span data-ttu-id="7c32a-147">지정 된 구독만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-147">Gets only the specified subscription.</span></span>
<span data-ttu-id="7c32a-148">구독 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-148">Enter the subscription name.</span></span>
<span data-ttu-id="7c32a-149">값은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-149">The value is case-sensitive.</span></span>
<span data-ttu-id="7c32a-150">와일드 카드 문자는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-150">Wildcard characters are not supported.</span></span>
<span data-ttu-id="7c32a-151">기본적으로 **Get-AzureSubscription** 는 Azure 계정의 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-151">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c32a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c32a-152">CommonParameters</span></span>
<span data-ttu-id="7c32a-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c32a-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c32a-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c32a-155">입력</span><span class="sxs-lookup"><span data-stu-id="7c32a-155">INPUTS</span></span>

### <span data-ttu-id="7c32a-156">않아야</span><span class="sxs-lookup"><span data-stu-id="7c32a-156">None</span></span>
<span data-ttu-id="7c32a-157">**SubscriptionName** 속성에는 이름을 기준으로 입력할 수 있지만 값으로는 파이프 하 여 입력 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-157">You can pipe input to the **SubscriptionName** property by name, but not by value.</span></span>

## <span data-ttu-id="7c32a-158">출력</span><span class="sxs-lookup"><span data-stu-id="7c32a-158">OUTPUTS</span></span>

### <span data-ttu-id="7c32a-159">WindowsAzure. 유틸리티. WindowsAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="7c32a-159">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureSubscription</span></span>

## <span data-ttu-id="7c32a-160">상속자</span><span class="sxs-lookup"><span data-stu-id="7c32a-160">NOTES</span></span>
* <span data-ttu-id="7c32a-161">Get-AzureSubscription 구독 데이터 파일에서 **-AzureAccount** 및 **가져오기-** 추가 작업 파일 cmdlet이 생성 하는 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c32a-161">Get-AzureSubscription gets data from the subscription data file that the **Add-AzureAccount** and **Import-PublishSettingsFile** cmdlets create.</span></span>

## <span data-ttu-id="7c32a-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c32a-162">RELATED LINKS</span></span>

[<span data-ttu-id="7c32a-163">추가-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="7c32a-163">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="7c32a-164">Get-Azure도움말 파일</span><span class="sxs-lookup"><span data-stu-id="7c32a-164">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="7c32a-165">가져오기-Azure# settingsfile</span><span class="sxs-lookup"><span data-stu-id="7c32a-165">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="7c32a-166">제거-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="7c32a-166">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="7c32a-167">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="7c32a-167">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


