---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: ac293211c332d8e99a592eedf96bbc179be99912
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044713"
---
# <span data-ttu-id="e3596-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e3596-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="e3596-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3596-102">SYNOPSIS</span></span>
<span data-ttu-id="e3596-103">Azure Site Recovery 자격 증명 모음 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3596-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="e3596-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e3596-104">SYNTAX</span></span>

### <span data-ttu-id="e3596-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="e3596-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3596-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="e3596-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3596-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="e3596-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3596-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e3596-108">DESCRIPTION</span></span>
<span data-ttu-id="e3596-109">**AzRecoveryServicesVaultSettingsFile** Cmdlet은 Azure Site Recovery 자격 증명 모음에 대 한 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3596-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="e3596-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e3596-110">EXAMPLES</span></span>

### <span data-ttu-id="e3596-111">예제 1: Windows Server 또는 Azure 백업용 DPM 컴퓨터 등록</span><span class="sxs-lookup"><span data-stu-id="e3596-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="e3596-112">첫 번째 명령은 TestVault 이라는 자격 증명 모음을 가져온 다음이를 $Vault 01 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3596-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="e3596-113">두 번째 명령은 $CredsPath 변수를 C:\Downloads.로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3596-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="e3596-114">마지막 명령은 Azure 백업용 $CredsPath의 자격 증명을 사용 하 여 $Vault 01에 대 한 자격 증명 모음 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3596-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="e3596-115">예제 2:</span><span class="sxs-lookup"><span data-stu-id="e3596-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="e3596-116">명령이 자격 증명 모음 형식 siteRecovery의 01 $Vault에 대 한 자격 증명 모음 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3596-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="e3596-117">예제 3: Windows Server 또는 Azure 백업용 DPM 컴퓨터 등록</span><span class="sxs-lookup"><span data-stu-id="e3596-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="e3596-118">명령 $Vault 01에 대 한 자격 증명 모음 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3596-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="e3596-119">변수</span><span class="sxs-lookup"><span data-stu-id="e3596-119">PARAMETERS</span></span>

### <span data-ttu-id="e3596-120">-백업</span><span class="sxs-lookup"><span data-stu-id="e3596-120">-Backup</span></span>
<span data-ttu-id="e3596-121">자격 증명 모음 파일을 Azure 백업에 적용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e3596-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultTypeWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3596-122">-인증서</span><span class="sxs-lookup"><span data-stu-id="e3596-122">-Certificate</span></span>
<span data-ttu-id="e3596-123">{{인증서 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="e3596-123">{{Fill Certificate Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3596-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3596-124">-DefaultProfile</span></span>
<span data-ttu-id="e3596-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3596-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3596-126">-Path</span><span class="sxs-lookup"><span data-stu-id="e3596-126">-Path</span></span>
<span data-ttu-id="e3596-127">Azure Site Recovery 자격 증명 모음 설정 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3596-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="e3596-128">Azure Site Recovery 자격 증명 모음 포털에서이 파일을 다운로드 하 여 로컬로 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3596-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3596-129">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e3596-129">-SiteFriendlyName</span></span>
<span data-ttu-id="e3596-130">사이트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3596-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="e3596-131">Hyper-v 사이트의 자격 증명 모음을 다운로드 하는 경우이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3596-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3596-132">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="e3596-132">-SiteIdentifier</span></span>
<span data-ttu-id="e3596-133">사이트 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3596-133">Specifies the site identifier.</span></span>
<span data-ttu-id="e3596-134">Hyper-v 사이트의 자격 증명 모음을 다운로드 하는 경우이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3596-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3596-135">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e3596-135">-SiteRecovery</span></span>
<span data-ttu-id="e3596-136">자격 증명 모음 파일을 Azure Site Recovery에 적용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e3596-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSiteWithCertificate, ByDefaultWithCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3596-137">-저장실</span><span class="sxs-lookup"><span data-stu-id="e3596-137">-Vault</span></span>
<span data-ttu-id="e3596-138">Azure Site Recovery 자격 증명 모음 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3596-138">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3596-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3596-139">CommonParameters</span></span>
<span data-ttu-id="e3596-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3596-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3596-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e3596-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3596-142">입력</span><span class="sxs-lookup"><span data-stu-id="e3596-142">INPUTS</span></span>

### <span data-ttu-id="e3596-143">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="e3596-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="e3596-144">출력</span><span class="sxs-lookup"><span data-stu-id="e3596-144">OUTPUTS</span></span>

### <span data-ttu-id="e3596-145">VaultSettingsFilePath를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="e3596-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="e3596-146">상속자</span><span class="sxs-lookup"><span data-stu-id="e3596-146">NOTES</span></span>

## <span data-ttu-id="e3596-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3596-147">RELATED LINKS</span></span>

[<span data-ttu-id="e3596-148">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e3596-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="e3596-149">새로운 AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e3596-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="e3596-150">제거-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e3596-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


