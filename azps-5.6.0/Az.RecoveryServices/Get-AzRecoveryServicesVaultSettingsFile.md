---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: b71da123933cd190038164b67d37fb81b0d5c973
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003179"
---
# <span data-ttu-id="71320-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="71320-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="71320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71320-102">SYNOPSIS</span></span>
<span data-ttu-id="71320-103">Azure Site Recovery 자격 증명 모음 설정 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="71320-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="71320-104">구문</span><span class="sxs-lookup"><span data-stu-id="71320-104">SYNTAX</span></span>

### <span data-ttu-id="71320-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="71320-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71320-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="71320-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71320-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="71320-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71320-108">설명</span><span class="sxs-lookup"><span data-stu-id="71320-108">DESCRIPTION</span></span>
<span data-ttu-id="71320-109">**Get-AzRecoveryServicesVaultSettingsFile** cmdlet은 Azure Site Recovery 자격 증명 모음에 대한 설정 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="71320-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="71320-110">예제</span><span class="sxs-lookup"><span data-stu-id="71320-110">EXAMPLES</span></span>

### <span data-ttu-id="71320-111">예제 1: Azure Backup용 Windows Server 또는 DPM 컴퓨터 등록</span><span class="sxs-lookup"><span data-stu-id="71320-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="71320-112">첫 번째 명령은 TestVault라는 자격 증명 모음을 얻은 다음, 해당 자격 증명 모음을 $Vault 01 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="71320-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="71320-113">두 번째 명령은 $CredsPath 변수를 C:\Downloads로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="71320-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="71320-114">마지막 명령은 Azure Backup용 자격 증명을 사용하여 $Vault 01에 $CredsPath 자격 증명 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="71320-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="71320-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="71320-115">Example 2</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="71320-116">명령은 자격 증명 모음 형식 siteRecovery의 자격 증명 모음 $Vault 01의 자격 증명 모음 자격 증명 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="71320-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="71320-117">예제 3: Azure Backup용 Windows Server 또는 DPM 컴퓨터 등록</span><span class="sxs-lookup"><span data-stu-id="71320-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="71320-118">명령은 자격 증명 모음 자격 증명 파일을 $Vault 01입니다.</span><span class="sxs-lookup"><span data-stu-id="71320-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="71320-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="71320-119">PARAMETERS</span></span>

### <span data-ttu-id="71320-120">-Backup</span><span class="sxs-lookup"><span data-stu-id="71320-120">-Backup</span></span>
<span data-ttu-id="71320-121">자격 증명 모음 자격 증명 파일이 Azure Backup에 적용할 수 있는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="71320-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

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

### <span data-ttu-id="71320-122">-인증서</span><span class="sxs-lookup"><span data-stu-id="71320-122">-Certificate</span></span>
<span data-ttu-id="71320-123">{{Fill Certificate Description}}</span><span class="sxs-lookup"><span data-stu-id="71320-123">{{Fill Certificate Description}}</span></span>

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

### <span data-ttu-id="71320-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71320-124">-DefaultProfile</span></span>
<span data-ttu-id="71320-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71320-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71320-126">-Path</span><span class="sxs-lookup"><span data-stu-id="71320-126">-Path</span></span>
<span data-ttu-id="71320-127">Azure Site Recovery 자격 증명 모음 설정 파일에 대한 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71320-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="71320-128">Azure Site Recovery 자격 증명 모음 포털에서 이 파일을 다운로드하고 로컬로 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71320-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="71320-129">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="71320-129">-SiteFriendlyName</span></span>
<span data-ttu-id="71320-130">사이트 친화적인 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71320-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="71320-131">자격 증명 모음 자격 증명을 다운로드하는 경우 이 매개 변수를 Hyper-V 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="71320-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="71320-132">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="71320-132">-SiteIdentifier</span></span>
<span data-ttu-id="71320-133">사이트 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71320-133">Specifies the site identifier.</span></span>
<span data-ttu-id="71320-134">자격 증명 모음 자격 증명을 다운로드하는 경우 이 매개 변수를 Hyper-V 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="71320-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="71320-135">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="71320-135">-SiteRecovery</span></span>
<span data-ttu-id="71320-136">자격 증명 모음 자격 증명 파일이 Azure Site Recovery에 적용할 수 있는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="71320-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

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

### <span data-ttu-id="71320-137">-Vault</span><span class="sxs-lookup"><span data-stu-id="71320-137">-Vault</span></span>
<span data-ttu-id="71320-138">Azure Site Recovery 자격 증명 모음 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71320-138">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="71320-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71320-139">CommonParameters</span></span>
<span data-ttu-id="71320-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="71320-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71320-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71320-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71320-142">입력</span><span class="sxs-lookup"><span data-stu-id="71320-142">INPUTS</span></span>

### <span data-ttu-id="71320-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="71320-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="71320-144">출력</span><span class="sxs-lookup"><span data-stu-id="71320-144">OUTPUTS</span></span>

### <span data-ttu-id="71320-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="71320-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="71320-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="71320-146">NOTES</span></span>

## <span data-ttu-id="71320-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71320-147">RELATED LINKS</span></span>

[<span data-ttu-id="71320-148">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="71320-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="71320-149">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="71320-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="71320-150">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="71320-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


