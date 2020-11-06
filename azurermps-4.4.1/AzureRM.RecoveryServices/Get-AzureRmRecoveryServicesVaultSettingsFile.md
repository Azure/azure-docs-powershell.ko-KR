---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 603cd65195f9e33c5006dcb4f2dc98ffc64aa7a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533887"
---
# <span data-ttu-id="ec682-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ec682-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="ec682-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec682-102">SYNOPSIS</span></span>
<span data-ttu-id="ec682-103">Azure Site Recovery 자격 증명 모음 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ec682-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec682-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec682-104">SYNTAX</span></span>

### <span data-ttu-id="ec682-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="ec682-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec682-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="ec682-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec682-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="ec682-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec682-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ec682-108">DESCRIPTION</span></span>
<span data-ttu-id="ec682-109">**AzureRmRecoveryServicesVaultSettingsFile** Cmdlet은 Azure Site Recovery 자격 증명 모음에 대 한 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ec682-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="ec682-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ec682-110">EXAMPLES</span></span>

### <span data-ttu-id="ec682-111">예제 1: Windows Server 또는 Azure 백업용 DPM 컴퓨터 등록</span><span class="sxs-lookup"><span data-stu-id="ec682-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="ec682-112">첫 번째 명령은 TestVault 이라는 자격 증명 모음을 가져온 다음이를 $Vault 01 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec682-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="ec682-113">두 번째 명령은 $CredsPath 변수를 C:\Downloads.로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec682-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>

<span data-ttu-id="ec682-114">마지막 명령은 Azure 백업용 $CredsPath의 자격 증명을 사용 하 여 $Vault 01에 대 한 자격 증명 모음 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ec682-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

## <span data-ttu-id="ec682-115">변수</span><span class="sxs-lookup"><span data-stu-id="ec682-115">PARAMETERS</span></span>

### <span data-ttu-id="ec682-116">-백업</span><span class="sxs-lookup"><span data-stu-id="ec682-116">-Backup</span></span>
<span data-ttu-id="ec682-117">자격 증명 모음 파일을 Azure 백업에 적용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ec682-117">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec682-118">-Path</span><span class="sxs-lookup"><span data-stu-id="ec682-118">-Path</span></span>
<span data-ttu-id="ec682-119">Azure Site Recovery 자격 증명 모음 설정 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec682-119">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="ec682-120">Azure Site Recovery 자격 증명 모음 포털에서이 파일을 다운로드 하 여 로컬로 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec682-120">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="ec682-121">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ec682-121">-SiteFriendlyName</span></span>
<span data-ttu-id="ec682-122">사이트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec682-122">Specifies the site friendly name.</span></span>
<span data-ttu-id="ec682-123">Hyper-v 사이트의 자격 증명 모음을 다운로드 하는 경우이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec682-123">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec682-124">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="ec682-124">-SiteIdentifier</span></span>
<span data-ttu-id="ec682-125">사이트 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec682-125">Specifies the site identifier.</span></span>
<span data-ttu-id="ec682-126">Hyper-v 사이트의 자격 증명 모음을 다운로드 하는 경우이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec682-126">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec682-127">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ec682-127">-SiteRecovery</span></span>
<span data-ttu-id="ec682-128">자격 증명 모음 파일을 Azure Site Recovery에 적용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ec682-128">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec682-129">-저장실</span><span class="sxs-lookup"><span data-stu-id="ec682-129">-Vault</span></span>
<span data-ttu-id="ec682-130">Azure Site Recovery 자격 증명 모음 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec682-130">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="ec682-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec682-131">-DefaultProfile</span></span>
<span data-ttu-id="ec682-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec682-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec682-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec682-133">CommonParameters</span></span>
<span data-ttu-id="ec682-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec682-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec682-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec682-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec682-136">입력</span><span class="sxs-lookup"><span data-stu-id="ec682-136">INPUTS</span></span>

### <span data-ttu-id="ec682-137">ARSVault</span><span class="sxs-lookup"><span data-stu-id="ec682-137">ARSVault</span></span>
<span data-ttu-id="ec682-138">' Vault ' 매개 변수는 파이프라인에서 ' ARSVault ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec682-138">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="ec682-139">출력</span><span class="sxs-lookup"><span data-stu-id="ec682-139">OUTPUTS</span></span>

### <span data-ttu-id="ec682-140">VaultSettingsFilePath를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="ec682-140">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="ec682-141">상속자</span><span class="sxs-lookup"><span data-stu-id="ec682-141">NOTES</span></span>

## <span data-ttu-id="ec682-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec682-142">RELATED LINKS</span></span>

[<span data-ttu-id="ec682-143">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ec682-143">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="ec682-144">새로운 AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ec682-144">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="ec682-145">제거-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ec682-145">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


