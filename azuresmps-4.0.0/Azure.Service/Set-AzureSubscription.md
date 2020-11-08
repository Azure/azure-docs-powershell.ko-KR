---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6185C6BA-460E-4EEA-B1EF-CD67629AA75E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51c20ef378cd2629ea96f236339a97172fb3038e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045950"
---
# <span data-ttu-id="ff449-101">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="ff449-101">Set-AzureSubscription</span></span>

## <span data-ttu-id="ff449-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff449-102">SYNOPSIS</span></span>
<span data-ttu-id="ff449-103">Azure 구독을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-103">Changes an Azure subscription.</span></span>

## <span data-ttu-id="ff449-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ff449-104">SYNTAX</span></span>

### <span data-ttu-id="ff449-105">UpdateSubscriptionByIdParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ff449-105">UpdateSubscriptionByIdParameterSetName (Default)</span></span>
```
Set-AzureSubscription -SubscriptionId <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ff449-106">UpdateSubscriptionByNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ff449-106">UpdateSubscriptionByNameParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ff449-107">AddSubscriptionParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ff449-107">AddSubscriptionParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> -SubscriptionId <String> -Certificate <X509Certificate2>
 [-ServiceEndpoint <String>] [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>]
 [-Context <AzureStorageContext>] [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff449-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ff449-108">DESCRIPTION</span></span>
<span data-ttu-id="ff449-109">**Set-AzureSubscription** Cmdlet은 Azure 구독 개체의 속성을 설정 하 고 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-109">The **Set-AzureSubscription** cmdlet establishes and changes the properties of an Azure subscription object.</span></span>
<span data-ttu-id="ff449-110">이 cmdlet을 사용 하 여 기본 구독이 아닌 Azure 구독에서 작동 하거나 현재 저장소 계정을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-110">You can use this cmdlet to work in an Azure subscription that is not your default subscription or to change your current storage account.</span></span>
<span data-ttu-id="ff449-111">현재 및 기본 구독에 대 한 자세한 내용은 **Select-AzureSubscription** cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ff449-111">For information about current and default subscriptions, see the **Select-AzureSubscription** cmdlet.</span></span>

<span data-ttu-id="ff449-112">이 cmdlet은 실제 Azure 구독이 아닌 Azure 구독 개체에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-112">This cmdlet operates on an Azure subscription object, not your actual Azure subscription.</span></span>
<span data-ttu-id="ff449-113">Azure 구독을 만들고 프로 비전 하려면 [Azure 포털](https://azure.microsoft.com/) ()을 방문 하세요 https://azure.microsoft.com/) .</span><span class="sxs-lookup"><span data-stu-id="ff449-113">To create and provision an Azure subscription, visit the [Azure Portal](https://azure.microsoft.com/) (https://azure.microsoft.com/).</span></span>

<span data-ttu-id="ff449-114">이 cmdlet은 Windows PowerShell에 Azure 계정을 추가 하는 데 **-AzureAccount** 또는 **Import-Azureaccount settingsfile** cmdlet을 사용할 때 생성 하는 구독 데이터 파일의 데이터를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-114">This cmdlet changes the data in the subscription data file that you create when you use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** cmdlet to add an Azure account to Windows PowerShell.</span></span>

<span data-ttu-id="ff449-115">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ff449-116">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="ff449-117">예제의</span><span class="sxs-lookup"><span data-stu-id="ff449-117">EXAMPLES</span></span>

### <span data-ttu-id="ff449-118">예제 1: 기존 subscription1 변경</span><span class="sxs-lookup"><span data-stu-id="ff449-118">Example 1: Change an existing subscription1</span></span>
```
C:\PS> $thumbprint = <Thumbprint-2>
C:\PS> $differentCert = Get-Item cert:\\CurrentUser\My\$thumbprint 
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $differentCert
```

<span data-ttu-id="ff449-119">이 예제에서는 ContosoEngineering 이라는 구독에 대 한 인증서를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-119">This example changes the certificate for the subscription named ContosoEngineering.</span></span>

### <span data-ttu-id="ff449-120">예제 2: 서비스 끝점 변경</span><span class="sxs-lookup"><span data-stu-id="ff449-120">Example 2: Change the service endpoint</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -ServiceEndpoint "https://management.core.contoso.com"
```

<span data-ttu-id="ff449-121">이 명령은 ContosoEngineering 구독에 대 한 사용자 지정 서비스 끝점을 추가 하거나 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-121">This command adds or changes a custom service endpoint for the ContosoEngineering subscription.</span></span>

### <span data-ttu-id="ff449-122">예제 3: 속성 값 지우기</span><span class="sxs-lookup"><span data-stu-id="ff449-122">Example 3: Clear property values</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $null -ResourceManagerEndpoint $Null
```

<span data-ttu-id="ff449-123">이 명령은 인증서 및 ResourceManagerEndpoint 속성의 값을 null ($Null)로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-123">This command sets the values of the Certificate and ResourceManagerEndpoint properties to null ($Null).</span></span>
<span data-ttu-id="ff449-124">이렇게 하면 다른 설정을 변경 하지 않고 해당 속성의 값이 지워집니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-124">This clears the values of those properties without changing other settings.</span></span>

### <span data-ttu-id="ff449-125">예제 4: 대체 구독 데이터 파일 사용</span><span class="sxs-lookup"><span data-stu-id="ff449-125">Example 4: Use an alternate subscription data file</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoFinance -SubscriptionDataFile C:\Azure\SubscriptionData.xml -CurrentStorageAccount ContosoStorage01
```

<span data-ttu-id="ff449-126">이 명령은 ContosoFinance 구독의 현재 저장소 계정을 ContosoStorage01으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-126">This command changes the current storage account of the ContosoFinance subscription to ContosoStorage01.</span></span>
<span data-ttu-id="ff449-127">이 명령은 **subscriptiondatafile** 파일 매개 변수를 사용 하 여 C:\Azure\SubscriptionData.xml subscription data 파일의 데이터를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-127">The command uses the **SubscriptionDataFile** parameter to change the data in the C:\Azure\SubscriptionData.xml subscription data file.</span></span>
<span data-ttu-id="ff449-128">기본적으로 **Set-AzureSubscription** 는 로밍 사용자 프로필의 기본 구독 데이터 파일을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-128">By default, **Set-AzureSubscription** uses the default subscription data file in your roaming user profile.</span></span>

## <span data-ttu-id="ff449-129">변수</span><span class="sxs-lookup"><span data-stu-id="ff449-129">PARAMETERS</span></span>

### <span data-ttu-id="ff449-130">-인증서</span><span class="sxs-lookup"><span data-stu-id="ff449-130">-Certificate</span></span>
```yaml
Type: X509Certificate2
Parameter Sets: UpdateSubscriptionByIdParameterSetName, UpdateSubscriptionByNameParameterSetName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: X509Certificate2
Parameter Sets: AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff449-131">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="ff449-131">-Context</span></span>
```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff449-132">-CurrentStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ff449-132">-CurrentStorageAccountName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff449-133">-환경</span><span class="sxs-lookup"><span data-stu-id="ff449-133">-Environment</span></span>
<span data-ttu-id="ff449-134">Azure 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-134">Specifies an Azure environment.</span></span>

<span data-ttu-id="ff449-135">Azure 환경에서 글로벌 Azure 용 AzureCloud 및 중국의 21Vianet이 운영 하는 Azure 용 AzureChinaCloud와 같은 Microsoft Azure의 독립 배포입니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-135">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="ff449-136">Azure Pack 및 WAPack cmdlet을 사용 하 여 온-프레미스 Azure 환경을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-136">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="ff449-137">자세한 내용은 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ()을 참조 하세요 https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ff449-137">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff449-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff449-138">-PassThru</span></span>
<span data-ttu-id="ff449-139">명령이 성공한 경우 $True를 반환 하 고 오류가 발생 하면 $False 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-139">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="ff449-140">기본적으로이 cmdlet은 출력을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-140">By default, this cmdlet does not return any output.</span></span>
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

### <span data-ttu-id="ff449-141">-프로필</span><span class="sxs-lookup"><span data-stu-id="ff449-141">-Profile</span></span>
<span data-ttu-id="ff449-142">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ff449-143">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ff449-144">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff449-144">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="ff449-145">계정과 연결 된 리소스 그룹에 대 한 데이터를 포함 하 여 Azure Resource Manager 데이터에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-145">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="ff449-146">Azure 리소스 관리자에 대 한 자세한 내용은 [Azure Resource Manager cmdlet](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) 및 [Windows PowerShell을 사용 하 여 리소스 관리자](https://go.microsoft.com/fwlink/?LinkID=394767)  ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="ff449-146">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

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

### <span data-ttu-id="ff449-147">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff449-147">-ServiceEndpoint</span></span>
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

### <span data-ttu-id="ff449-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff449-148">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByIdParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff449-149">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ff449-149">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByNameParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff449-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff449-150">CommonParameters</span></span>
<span data-ttu-id="ff449-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff449-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff449-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff449-153">입력</span><span class="sxs-lookup"><span data-stu-id="ff449-153">INPUTS</span></span>

### <span data-ttu-id="ff449-154">않아야</span><span class="sxs-lookup"><span data-stu-id="ff449-154">None</span></span>
<span data-ttu-id="ff449-155">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-155">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="ff449-156">출력</span><span class="sxs-lookup"><span data-stu-id="ff449-156">OUTPUTS</span></span>

### <span data-ttu-id="ff449-157">없음 또는 시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ff449-157">None or System.Boolean</span></span>
<span data-ttu-id="ff449-158">*PassThru* 매개 변수를 사용 하는 경우이 Cmdlet은 부울 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-158">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="ff449-159">기본적으로이 cmdlet은 출력을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff449-159">By default, this cmdlet does not return any output.</span></span>

## <span data-ttu-id="ff449-160">상속자</span><span class="sxs-lookup"><span data-stu-id="ff449-160">NOTES</span></span>

## <span data-ttu-id="ff449-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff449-161">RELATED LINKS</span></span>

[<span data-ttu-id="ff449-162">추가-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="ff449-162">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="ff449-163">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="ff449-163">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="ff449-164">가져오기-Azure# settingsfile</span><span class="sxs-lookup"><span data-stu-id="ff449-164">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="ff449-165">제거-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="ff449-165">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="ff449-166">선택-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="ff449-166">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)


