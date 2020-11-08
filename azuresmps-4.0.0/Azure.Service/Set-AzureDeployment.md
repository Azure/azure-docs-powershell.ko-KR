---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7F51F534-6C64-4983-A08F-4732A39C2E7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c62f3d29b4cd2c87fd5606ca013eb03958fb62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046064"
---
# <span data-ttu-id="6bb91-101">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="6bb91-101">Set-AzureDeployment</span></span>

## <span data-ttu-id="6bb91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bb91-102">SYNOPSIS</span></span>
<span data-ttu-id="6bb91-103">배포의 상태, 구성 설정 또는 업그레이드 모드를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-103">Modifies the status, configuration settings, or upgrade mode of a deployment.</span></span>

## <span data-ttu-id="6bb91-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6bb91-104">SYNTAX</span></span>

### <span data-ttu-id="6bb91-105">업그레이드</span><span class="sxs-lookup"><span data-stu-id="6bb91-105">Upgrade</span></span>
```
Set-AzureDeployment [-Upgrade] [-ServiceName] <String> [-Package] <String> [-Configuration] <String>
 [-Slot] <String> [[-Mode] <String>] [[-Label] <String>] [[-RoleName] <String>] [-Force]
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6bb91-106">구성</span><span class="sxs-lookup"><span data-stu-id="6bb91-106">Config</span></span>
```
Set-AzureDeployment [-Config] [-ServiceName] <String> [-Configuration] <String> [-Slot] <String>
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6bb91-107">상태</span><span class="sxs-lookup"><span data-stu-id="6bb91-107">Status</span></span>
```
Set-AzureDeployment [-Status] [-ServiceName] <String> [-Slot] <String> [-NewStatus] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="6bb91-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6bb91-108">DESCRIPTION</span></span>
<span data-ttu-id="6bb91-109">**Set AzureDeployment** Cmdlet은 Azure 배포의 상태, 구성 설정 또는 업그레이드 모드를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-109">The **Set-AzureDeployment** cmdlet modifies the status, configuration settings, or upgrade mode of an Azure deployment.</span></span>
<span data-ttu-id="6bb91-110">배포 상태를 실행 중 또는 일시 중단으로 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-110">You can change the status of the deployment to either Running or Suspended.</span></span>
<span data-ttu-id="6bb91-111">배포에 대 한 .cscfg 파일을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-111">You can change the .cscfg file for the deployment.</span></span>
<span data-ttu-id="6bb91-112">업그레이드 모드를 설정 하 고 구성 파일을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-112">You can set the upgrade mode and update configuration files.</span></span>
<span data-ttu-id="6bb91-113">**AzureWalkUpgradeDomain** cmdlet을 사용 하 여 업그레이드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-113">Use the **Set-AzureWalkUpgradeDomain** cmdlet to initiate an upgrade.</span></span>

## <span data-ttu-id="6bb91-114">예제의</span><span class="sxs-lookup"><span data-stu-id="6bb91-114">EXAMPLES</span></span>

### <span data-ttu-id="6bb91-115">예제 1: 배포 상태 변경</span><span class="sxs-lookup"><span data-stu-id="6bb91-115">Example 1: Change the status of a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Status -ServiceName "ContosoService" -Slot "Production" -NewStatus "Running"
```

<span data-ttu-id="6bb91-116">이 명령은 프로덕션 환경에서 ContosoService 라는 서비스에 대 한 배포의 상태를 실행 중으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-116">This command sets the status of the deployment for the service named ContosoService in the production environment to Running.</span></span>

### <span data-ttu-id="6bb91-117">예제 2: 배포에 다른 구성 파일 할당</span><span class="sxs-lookup"><span data-stu-id="6bb91-117">Example 2: Assign a different configuration file to a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Slot "Staging" -Configuration "C:\Temp\MyServiceConfig.Cloud.csfg"
```

<span data-ttu-id="6bb91-118">이 명령은 스테이징 환경에서 ContosoService 이라는 서비스에 대 한 배포에 대해 다른 구성 파일을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-118">This command assigns a different configuration file for the deployment for the service named ContosoService in the staging environment.</span></span>

### <span data-ttu-id="6bb91-119">예제 3: 업그레이드 모드를 자동으로 설정</span><span class="sxs-lookup"><span data-stu-id="6bb91-119">Example 3: Set the upgrade mode to Auto</span></span>
```
PS C:\> Set-AzureDeployment -Upgrade -ServiceName "ContosoService" -Mode Auto -Package "C:\packages\ContosoApp.cspkg" -Configuration "C:\Config\ContosoServiceConfig.Cloud.csfg"
```

<span data-ttu-id="6bb91-120">이 명령은 업그레이드 모드를 Auto로 설정 하 고 업그레이드 패키지와 새 구성 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-120">This command sets the upgrade mode to Auto, and specifies an upgrade package and a new configuration file.</span></span>

### <span data-ttu-id="6bb91-121">예제 4: 서비스에 확장 구성 설치</span><span class="sxs-lookup"><span data-stu-id="6bb91-121">Example 4: Install extension configuration in a service</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Mode "Automatic" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Slot "Production" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="6bb91-122">이 명령은 지정 된 클라우드 서비스에 확장 구성을 설치 하 고 역할에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-122">This command installs the extension configuration in the specified Cloud Service and applies them on roles.</span></span>

## <span data-ttu-id="6bb91-123">변수</span><span class="sxs-lookup"><span data-stu-id="6bb91-123">PARAMETERS</span></span>

### <span data-ttu-id="6bb91-124">-구성</span><span class="sxs-lookup"><span data-stu-id="6bb91-124">-Config</span></span>
<span data-ttu-id="6bb91-125">이 cmdlet이 배포의 구성을 수정 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-125">Specifies that this cmdlet modifies the configuration of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Config
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb91-126">-구성</span><span class="sxs-lookup"><span data-stu-id="6bb91-126">-Configuration</span></span>
<span data-ttu-id="6bb91-127">.Cscfg 구성 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-127">Specifies the full path of a .cscfg configuration file.</span></span>
<span data-ttu-id="6bb91-128">업그레이드 또는 구성 변경에 대 한 구성 파일을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-128">You can specify a configuration file for an upgrade or configuration change.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade, Config
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb91-129">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bb91-129">-ExtensionConfiguration</span></span>
<span data-ttu-id="6bb91-130">확장 구성 개체의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-130">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: Upgrade, Config
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bb91-131">-Force</span><span class="sxs-lookup"><span data-stu-id="6bb91-131">-Force</span></span>
<span data-ttu-id="6bb91-132">Cmdlet이 강제로 업그레이드를 수행 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-132">Indicates that cmdlet performs a forced upgrade.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb91-133">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6bb91-133">-InformationAction</span></span>
<span data-ttu-id="6bb91-134">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-134">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6bb91-135">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6bb91-136">하기로</span><span class="sxs-lookup"><span data-stu-id="6bb91-136">Continue</span></span>
- <span data-ttu-id="6bb91-137">숨기기</span><span class="sxs-lookup"><span data-stu-id="6bb91-137">Ignore</span></span>
- <span data-ttu-id="6bb91-138">Inquire</span><span class="sxs-lookup"><span data-stu-id="6bb91-138">Inquire</span></span>
- <span data-ttu-id="6bb91-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6bb91-139">SilentlyContinue</span></span>
- <span data-ttu-id="6bb91-140">중지가</span><span class="sxs-lookup"><span data-stu-id="6bb91-140">Stop</span></span>
- <span data-ttu-id="6bb91-141">대기</span><span class="sxs-lookup"><span data-stu-id="6bb91-141">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb91-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6bb91-142">-InformationVariable</span></span>
<span data-ttu-id="6bb91-143">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-143">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb91-144">-레이블</span><span class="sxs-lookup"><span data-stu-id="6bb91-144">-Label</span></span>
<span data-ttu-id="6bb91-145">업그레이드 된 배포의 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-145">Specifies a label for the upgraded deployment.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb91-146">-모드</span><span class="sxs-lookup"><span data-stu-id="6bb91-146">-Mode</span></span>
<span data-ttu-id="6bb91-147">업그레이드 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-147">Specifies the mode of upgrade.</span></span>
<span data-ttu-id="6bb91-148">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-148">Valid values are:</span></span> 

- <span data-ttu-id="6bb91-149">자동</span><span class="sxs-lookup"><span data-stu-id="6bb91-149">Auto</span></span> 
- <span data-ttu-id="6bb91-150">수동</span><span class="sxs-lookup"><span data-stu-id="6bb91-150">Manual</span></span> 
- <span data-ttu-id="6bb91-151">연립</span><span class="sxs-lookup"><span data-stu-id="6bb91-151">Simultaneous</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb91-152">-새 상태</span><span class="sxs-lookup"><span data-stu-id="6bb91-152">-NewStatus</span></span>
<span data-ttu-id="6bb91-153">배포의 대상 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-153">Specifies the target status for the deployment.</span></span>
<span data-ttu-id="6bb91-154">유효한 값은 실행 중이 고 일시 중단 됨입니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-154">Valid values are: Running and Suspended.</span></span>

```yaml
Type: String
Parameter Sets: Status
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb91-155">-패키지</span><span class="sxs-lookup"><span data-stu-id="6bb91-155">-Package</span></span>
<span data-ttu-id="6bb91-156">업그레이드 패키지 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-156">Specifies the full path of an upgrade package file.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb91-157">-프로필</span><span class="sxs-lookup"><span data-stu-id="6bb91-157">-Profile</span></span>
<span data-ttu-id="6bb91-158">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-158">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6bb91-159">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-159">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6bb91-160">-RoleName</span><span class="sxs-lookup"><span data-stu-id="6bb91-160">-RoleName</span></span>
<span data-ttu-id="6bb91-161">업그레이드할 역할의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-161">Specifies the name of the role to upgrade.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb91-162">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6bb91-162">-ServiceName</span></span>
<span data-ttu-id="6bb91-163">배포에 대 한 Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-163">Specifies the name of the Azure service of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bb91-164">-슬롯</span><span class="sxs-lookup"><span data-stu-id="6bb91-164">-Slot</span></span>
<span data-ttu-id="6bb91-165">수정할 배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-165">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="6bb91-166">유효한 값은 프로덕션 및 준비입니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-166">Valid values are: Production and Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bb91-167">-상태</span><span class="sxs-lookup"><span data-stu-id="6bb91-167">-Status</span></span>
<span data-ttu-id="6bb91-168">이 cmdlet이 배포의 상태를 변경 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-168">Specifies that this cmdlet changes the status of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Status
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb91-169">-업그레이드</span><span class="sxs-lookup"><span data-stu-id="6bb91-169">-Upgrade</span></span>
<span data-ttu-id="6bb91-170">이 cmdlet이 배포를 업그레이드 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-170">Specifies that this cmdlet upgrades the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb91-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bb91-171">CommonParameters</span></span>
<span data-ttu-id="6bb91-172">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb91-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bb91-173">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bb91-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bb91-174">입력</span><span class="sxs-lookup"><span data-stu-id="6bb91-174">INPUTS</span></span>

## <span data-ttu-id="6bb91-175">출력</span><span class="sxs-lookup"><span data-stu-id="6bb91-175">OUTPUTS</span></span>

## <span data-ttu-id="6bb91-176">상속자</span><span class="sxs-lookup"><span data-stu-id="6bb91-176">NOTES</span></span>

## <span data-ttu-id="6bb91-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6bb91-177">RELATED LINKS</span></span>

[<span data-ttu-id="6bb91-178">다운로드-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="6bb91-178">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="6bb91-179">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="6bb91-179">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="6bb91-180">이동-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="6bb91-180">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="6bb91-181">새 AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="6bb91-181">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="6bb91-182">-AzureDeployment 제거</span><span class="sxs-lookup"><span data-stu-id="6bb91-182">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="6bb91-183">Set-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="6bb91-183">Set-AzureWalkUpgradeDomain</span></span>](./Set-AzureWalkUpgradeDomain.md)


