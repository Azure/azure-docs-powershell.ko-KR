---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045883"
---
# <span data-ttu-id="aaacd-101">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="aaacd-101">Publish-AzureServiceProject</span></span>

## <span data-ttu-id="aaacd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaacd-102">SYNOPSIS</span></span>
<span data-ttu-id="aaacd-103">현재 서비스를 Windows Azure에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-103">Publish the current service to Windows Azure.</span></span>

## <span data-ttu-id="aaacd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aaacd-104">SYNTAX</span></span>

### <span data-ttu-id="aaacd-105"># 정의 (기본값)</span><span class="sxs-lookup"><span data-stu-id="aaacd-105">PublishFromServiceDefinition (Default)</span></span>
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="aaacd-106">패키지</span><span class="sxs-lookup"><span data-stu-id="aaacd-106">PublishFromPackage</span></span>
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="aaacd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="aaacd-107">DESCRIPTION</span></span>
<span data-ttu-id="aaacd-108">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="aaacd-109">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="aaacd-110">**게시-AzureServiceProject** cmdlet은 현재 서비스를 클라우드에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-110">The **Publish-AzureServiceProject** cmdlet publishes the current service to the cloud.</span></span>
<span data-ttu-id="aaacd-111">게시 구성 (예: **구독** , **storageaccountname** , **Location** , **Slot** 등)을 명령줄에 지정 하거나 **Set-azureserviceproject** cmdlet을 통해 로컬 설정에 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-111">You can specify publishing configuration (such as **Subscription** , **StorageAccountName** , **Location** , **Slot** ) on the command line, or in local settings through the **Set-AzureServiceProject** cmdlet.</span></span>

## <span data-ttu-id="aaacd-112">예제의</span><span class="sxs-lookup"><span data-stu-id="aaacd-112">EXAMPLES</span></span>

### <span data-ttu-id="aaacd-113">예제 1: 기본 값을 사용 하 여 서비스 프로젝트 게시</span><span class="sxs-lookup"><span data-stu-id="aaacd-113">Example 1: Publish a service project with default values</span></span>
```
PS C:\> Publish-AzureServiceProject
```

<span data-ttu-id="aaacd-114">이 예제에서는 현재 서비스 설정 및 현재 Azure 게시 프로필을 사용 하 여 현재 서비스를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-114">This example publishes the current service, using the current service settings and the current Azure publish profile.</span></span>

### <span data-ttu-id="aaacd-115">예제 2: 배포 패키지 만들기</span><span class="sxs-lookup"><span data-stu-id="aaacd-115">Example 2: Create a deployment package</span></span>
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

<span data-ttu-id="aaacd-116">이 예제에서는 서비스 디렉터리에 배포 패키지 (cspkg) 파일을 만들고, Windows Azure에 게시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-116">This example creates a deployment package (.cspkg) file in the service directory and does not publish to Windows Azure.</span></span>

## <span data-ttu-id="aaacd-117">변수</span><span class="sxs-lookup"><span data-stu-id="aaacd-117">PARAMETERS</span></span>

### <span data-ttu-id="aaacd-118">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="aaacd-118">-AffinityGroup</span></span>
<span data-ttu-id="aaacd-119">서비스에 사용 하려는 선호도 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-119">Specifies the affinity group that you want the service to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaacd-120">-구성</span><span class="sxs-lookup"><span data-stu-id="aaacd-120">-Configuration</span></span>
<span data-ttu-id="aaacd-121">서비스 구성 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-121">Specifies the service configuration file.</span></span>
<span data-ttu-id="aaacd-122">이 매개 변수를 지정 하는 경우 *Package* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-122">If you specify this parameter, specify the *Package* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaacd-123">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="aaacd-123">-DeploymentName</span></span>
<span data-ttu-id="aaacd-124">배포 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-124">Specifies the deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaacd-125">-ForceUpgrade</span><span class="sxs-lookup"><span data-stu-id="aaacd-125">-ForceUpgrade</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaacd-126">-시작</span><span class="sxs-lookup"><span data-stu-id="aaacd-126">-Launch</span></span>
<span data-ttu-id="aaacd-127">응용 프로그램이 배포 된 후 볼 수 있도록 브라우저 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-127">Opens a browser window so you can view the application after it is deployed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaacd-128">-위치</span><span class="sxs-lookup"><span data-stu-id="aaacd-128">-Location</span></span>
<span data-ttu-id="aaacd-129">응용 프로그램이 호스팅되는 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-129">The region in which the application will be hosted.</span></span>
<span data-ttu-id="aaacd-130">사용할 수 있는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-130">Possible values are:</span></span> 
  
- <span data-ttu-id="aaacd-131">아시아 어디서 나</span><span class="sxs-lookup"><span data-stu-id="aaacd-131">Anywhere Asia</span></span>
- <span data-ttu-id="aaacd-132">유럽 어디서 나</span><span class="sxs-lookup"><span data-stu-id="aaacd-132">Anywhere Europe</span></span>
- <span data-ttu-id="aaacd-133">미국 어디서 나</span><span class="sxs-lookup"><span data-stu-id="aaacd-133">Anywhere US</span></span>
- <span data-ttu-id="aaacd-134">동아시아</span><span class="sxs-lookup"><span data-stu-id="aaacd-134">East Asia</span></span>
- <span data-ttu-id="aaacd-135">미국 동부</span><span class="sxs-lookup"><span data-stu-id="aaacd-135">East US</span></span>
- <span data-ttu-id="aaacd-136">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="aaacd-136">North Central US</span></span>
- <span data-ttu-id="aaacd-137">동유럽</span><span class="sxs-lookup"><span data-stu-id="aaacd-137">North Europe</span></span>
- <span data-ttu-id="aaacd-138">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="aaacd-138">South Central US</span></span>
- <span data-ttu-id="aaacd-139">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="aaacd-139">Southeast Asia</span></span>
- <span data-ttu-id="aaacd-140">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="aaacd-140">West Europe</span></span>
- <span data-ttu-id="aaacd-141">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="aaacd-141">West US</span></span>
 
<span data-ttu-id="aaacd-142">위치를 지정 하지 않으면 **Set-AzureServiceProject** 에 대 한 마지막 호출에 지정 된 위치가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-142">If no Location is specified, the location specified in the last call to **Set-AzureServiceProject** will be used.</span></span> <span data-ttu-id="aaacd-143">지정 된 위치가 없으면 위치는 ' 미국 중부 US ' 및 ' 남 중부 US ' 위치에서 임의로 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-143">If no Location was ever specified, the Location will be randomly chosen from 'North Central US' and 'South Central US' locations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaacd-144">-패키지</span><span class="sxs-lookup"><span data-stu-id="aaacd-144">-Package</span></span>
<span data-ttu-id="aaacd-145">배포할 패키지 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-145">Specifies the package file to deploy.</span></span>
<span data-ttu-id="aaacd-146">Cspkg 파일 이름 확장명을 가진 로컬 파일 또는 패키지를 포함 하는 blob의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-146">Specify either a local file that has the .cspkg file name extension or a URI of a blob that contains the package.</span></span>
<span data-ttu-id="aaacd-147">이 매개 변수를 지정 하는 경우 *ServiceName* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="aaacd-147">If you specify this parameter, do not specify the *ServiceName* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaacd-148">-프로필</span><span class="sxs-lookup"><span data-stu-id="aaacd-148">-Profile</span></span>
<span data-ttu-id="aaacd-149">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aaacd-150">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aaacd-151">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="aaacd-151">-ServiceName</span></span>
<span data-ttu-id="aaacd-152">Windows Azure에 게시할 때 서비스에 사용할 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-152">Specifies the name to be used for the service when publishing to Windows Azure.</span></span>
<span data-ttu-id="aaacd-153">이름은 cloudapp.net 하위 도메인에서 Windows Azure (cloudapp.net)에 호스트 되는 서비스를 처리 하는 데 사용 되는 레이블의 **일부를 결정** 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-153">The name determines part of the label in the cloudapp.net subdomain that is used to address the service when hosted in Windows Azure (that is, **name**.cloudapp.net).</span></span>
<span data-ttu-id="aaacd-154">서비스를 게시 하는 동안 지정 된 이름은 서비스를 만들 때 지정 된 이름 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-154">Any name specified while publishing the service overrides the name given when the service was created.</span></span>
<span data-ttu-id="aaacd-155">( **새-AzureServiceProject** cmdlet을 참조 하세요.)</span><span class="sxs-lookup"><span data-stu-id="aaacd-155">(See the **New-AzureServiceProject** cmdlet).</span></span>

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaacd-156">-슬롯</span><span class="sxs-lookup"><span data-stu-id="aaacd-156">-Slot</span></span>
<span data-ttu-id="aaacd-157">이 서비스에 사용할 배포 슬롯입니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-157">The deployment slot to be used for this service.</span></span>
<span data-ttu-id="aaacd-158">사용할 수 있는 값은 ' 준비 ' 및 ' 생산 '입니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-158">Possible values are 'Staging' and 'Production'.</span></span>
<span data-ttu-id="aaacd-159">슬롯을 지정 하지 않으면 Set-AzureDeploymentSlot에 대 한 마지막 호출에 제공 된 슬롯이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-159">If no slot is specified, the slot provided in the last call to Set-AzureDeploymentSlot is used.</span></span>
<span data-ttu-id="aaacd-160">슬롯이 지정 되지 않은 경우 ' 제작 ' 슬롯이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-160">If no slot has ever been specified, the 'Production' slot is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaacd-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="aaacd-161">-StorageAccountName</span></span>
<span data-ttu-id="aaacd-162">서비스를 게시 하는 동안 사용할 Windows Azure 저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-162">Specifies the Windows Azure storage account name to be used while publishing the service.</span></span>
<span data-ttu-id="aaacd-163">이 값은 서비스가 게시 될 때까지 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-163">This value is not used until the service is published.</span></span>
<span data-ttu-id="aaacd-164">이 매개 변수를 지정 하지 않으면 마지막 **집합-AzureServiceProject** 명령에서 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-164">When this parameter is not specified, the value is obtained from the last **Set-AzureServiceProject** command.</span></span>
<span data-ttu-id="aaacd-165">저장소 계정이 지정 되지 않은 경우 서비스 이름과 일치 하는 저장소 계정이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-165">If no storage account was ever specified, a storage account matching the name of the service will be used.</span></span>
<span data-ttu-id="aaacd-166">이러한 저장소 계정이 없는 경우 cmdlet은 새 계정을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-166">If no such storage account exists, the cmdlet attempts to create a new one.</span></span>
<span data-ttu-id="aaacd-167">그러나 서비스 이름과 일치 하는 저장소 계정이 다른 구독에 있으면 시도가 실패할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-167">However, the attempt may fail if a storage account matching the service name exists in another subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaacd-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaacd-168">CommonParameters</span></span>
<span data-ttu-id="aaacd-169">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaacd-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaacd-170">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaacd-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaacd-171">입력</span><span class="sxs-lookup"><span data-stu-id="aaacd-171">INPUTS</span></span>

## <span data-ttu-id="aaacd-172">출력</span><span class="sxs-lookup"><span data-stu-id="aaacd-172">OUTPUTS</span></span>

## <span data-ttu-id="aaacd-173">상속자</span><span class="sxs-lookup"><span data-stu-id="aaacd-173">NOTES</span></span>

## <span data-ttu-id="aaacd-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aaacd-174">RELATED LINKS</span></span>

[<span data-ttu-id="aaacd-175">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="aaacd-175">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)

[<span data-ttu-id="aaacd-176">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="aaacd-176">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


