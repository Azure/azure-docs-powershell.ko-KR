---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: b272f22c0bac37f5318deff50f1f0b56a849ce2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703558"
---
# <span data-ttu-id="c634d-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="c634d-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="c634d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c634d-102">SYNOPSIS</span></span>
<span data-ttu-id="c634d-103">Azure Site Recovery 자격 증명 모음 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c634d-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c634d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c634d-104">SYNTAX</span></span>

### <span data-ttu-id="c634d-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="c634d-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c634d-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="c634d-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c634d-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="c634d-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c634d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c634d-108">DESCRIPTION</span></span>
<span data-ttu-id="c634d-109">**AzureRmRecoveryServicesVaultSettingsFile** Cmdlet은 Azure Site Recovery 자격 증명 모음에 대 한 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c634d-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="c634d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c634d-110">EXAMPLES</span></span>

### <span data-ttu-id="c634d-111">예제 1: Windows Server 또는 Azure 백업용 DPM 컴퓨터 등록</span><span class="sxs-lookup"><span data-stu-id="c634d-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="c634d-112">첫 번째 명령은 TestVault 이라는 자격 증명 모음을 가져온 다음이를 $Vault 01 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c634d-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="c634d-113">두 번째 명령은 $CredsPath 변수를 C:\Downloads.로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c634d-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>

<span data-ttu-id="c634d-114">마지막 명령은 Azure 백업용 $CredsPath의 자격 증명을 사용 하 여 $Vault 01에 대 한 자격 증명 모음 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c634d-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="c634d-115">예제 2:</span><span class="sxs-lookup"><span data-stu-id="c634d-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="c634d-116">명령이 자격 증명 모음 형식 siteRecovery의 01 $Vault에 대 한 자격 증명 모음 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c634d-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="c634d-117">예제 3: Windows Server 또는 Azure 백업용 DPM 컴퓨터 등록</span><span class="sxs-lookup"><span data-stu-id="c634d-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="c634d-118">명령 $Vault 01에 대 한 자격 증명 모음 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c634d-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="c634d-119">변수</span><span class="sxs-lookup"><span data-stu-id="c634d-119">PARAMETERS</span></span>

### <span data-ttu-id="c634d-120">-백업</span><span class="sxs-lookup"><span data-stu-id="c634d-120">-Backup</span></span>
<span data-ttu-id="c634d-121">자격 증명 모음 파일을 Azure 백업에 적용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c634d-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c634d-122">-Path</span><span class="sxs-lookup"><span data-stu-id="c634d-122">-Path</span></span>
<span data-ttu-id="c634d-123">Azure Site Recovery 자격 증명 모음 설정 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c634d-123">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="c634d-124">Azure Site Recovery 자격 증명 모음 포털에서이 파일을 다운로드 하 여 로컬로 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c634d-124">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c634d-125">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c634d-125">-SiteFriendlyName</span></span>
<span data-ttu-id="c634d-126">사이트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c634d-126">Specifies the site friendly name.</span></span>
<span data-ttu-id="c634d-127">Hyper-v 사이트의 자격 증명 모음을 다운로드 하는 경우이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c634d-127">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c634d-128">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="c634d-128">-SiteIdentifier</span></span>
<span data-ttu-id="c634d-129">사이트 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c634d-129">Specifies the site identifier.</span></span>
<span data-ttu-id="c634d-130">Hyper-v 사이트의 자격 증명 모음을 다운로드 하는 경우이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c634d-130">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c634d-131">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c634d-131">-SiteRecovery</span></span>
<span data-ttu-id="c634d-132">자격 증명 모음 파일을 Azure Site Recovery에 적용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c634d-132">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c634d-133">-저장실</span><span class="sxs-lookup"><span data-stu-id="c634d-133">-Vault</span></span>
<span data-ttu-id="c634d-134">Azure Site Recovery 자격 증명 모음 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c634d-134">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c634d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c634d-135">-DefaultProfile</span></span>
<span data-ttu-id="c634d-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c634d-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c634d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c634d-137">CommonParameters</span></span>
<span data-ttu-id="c634d-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c634d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c634d-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c634d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c634d-140">입력</span><span class="sxs-lookup"><span data-stu-id="c634d-140">INPUTS</span></span>

### <span data-ttu-id="c634d-141">ARSVault</span><span class="sxs-lookup"><span data-stu-id="c634d-141">ARSVault</span></span>
<span data-ttu-id="c634d-142">' Vault ' 매개 변수는 파이프라인에서 ' ARSVault ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c634d-142">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="c634d-143">출력</span><span class="sxs-lookup"><span data-stu-id="c634d-143">OUTPUTS</span></span>

### <span data-ttu-id="c634d-144">VaultSettingsFilePath를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="c634d-144">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="c634d-145">상속자</span><span class="sxs-lookup"><span data-stu-id="c634d-145">NOTES</span></span>

## <span data-ttu-id="c634d-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c634d-146">RELATED LINKS</span></span>

[<span data-ttu-id="c634d-147">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="c634d-147">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="c634d-148">새로운 AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="c634d-148">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="c634d-149">제거-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="c634d-149">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


