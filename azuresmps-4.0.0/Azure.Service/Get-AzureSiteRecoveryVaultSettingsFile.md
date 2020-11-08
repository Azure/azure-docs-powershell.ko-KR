---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AFAA1BDF-3F6A-437A-ADC2-C5EBD970F57D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e86fdb7f1e995af71e09bdce17754b11819bec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046564"
---
# <span data-ttu-id="1f86b-101">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1f86b-101">Get-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="1f86b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f86b-102">SYNOPSIS</span></span>
<span data-ttu-id="1f86b-103">사이트 복구 자격 증명 모음 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f86b-103">Gets the Site Recovery vault settings file.</span></span>

## <span data-ttu-id="1f86b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f86b-104">SYNTAX</span></span>

### <span data-ttu-id="1f86b-105">ByParam (기본값)</span><span class="sxs-lookup"><span data-stu-id="1f86b-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Name <String> -Location <String> [-SiteName <String>]
 [-SiteId <String>] [-Path <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1f86b-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="1f86b-106">ByObject</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Site <ASRSite>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f86b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1f86b-107">DESCRIPTION</span></span>
<span data-ttu-id="1f86b-108">**AzureSiteRecoveryVaultSettingsFile** Cmdlet은 Azure Site Recovery 자격 증명 모음에 대 한 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f86b-108">The **Get-AzureSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="1f86b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1f86b-109">EXAMPLES</span></span>

### <span data-ttu-id="1f86b-110">예제 1: 자격 증명 모음에 대 한 설정 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="1f86b-110">Example 1: Get the settings file for a vault</span></span>
```
PS C:\> $Vault = Get-AzureSiteRecoveryVault -Name "ContosoVault"
PS C:\> Get-AzureSiteRecoveryVaultSettingsFile -Vault $Vault
FilePath 
-------- 
C:\Users\ContosoAdmin\ContosoVault_2015-02-02T05-39-23.VaultCredentials
```

<span data-ttu-id="1f86b-111">첫 번째 명령은 **AzureSiteRecoveryVault** cmdlet을 사용 하 여 ContosoVault 이라는 활성 Azure Site Recovery 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f86b-111">The first command gets the active Azure Site Recovery vault named ContosoVault by using the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>
<span data-ttu-id="1f86b-112">명령이 $Vault 변수에 해당 자격 증명을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f86b-112">The command stores that vault in the $Vault variable.</span></span>

<span data-ttu-id="1f86b-113">두 번째 명령은 $Vault에 저장 된 보관소에 대 한 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f86b-113">The second command gets the settings file for the vault stored in $Vault.</span></span>

## <span data-ttu-id="1f86b-114">변수</span><span class="sxs-lookup"><span data-stu-id="1f86b-114">PARAMETERS</span></span>

### <span data-ttu-id="1f86b-115">-위치</span><span class="sxs-lookup"><span data-stu-id="1f86b-115">-Location</span></span>
<span data-ttu-id="1f86b-116">보관소가 속한 지리적 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f86b-116">Specifies the geographical location to which the vault belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f86b-117">-이름</span><span class="sxs-lookup"><span data-stu-id="1f86b-117">-Name</span></span>
<span data-ttu-id="1f86b-118">자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f86b-118">Specifies the name of a vault.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f86b-119">-Path</span><span class="sxs-lookup"><span data-stu-id="1f86b-119">-Path</span></span>
<span data-ttu-id="1f86b-120">사이트 복구 자격 증명 모음 설정 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f86b-120">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="1f86b-121">이 파일을 로컬로 저장 하려면 명령이 실행을 완료 한 후 사이트 복구 자격 증명 모음 포털에서 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f86b-121">To store this file locally, download it from the Site Recovery vault portal after the command has finished running.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f86b-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="1f86b-122">-Profile</span></span>
<span data-ttu-id="1f86b-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f86b-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1f86b-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="1f86b-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1f86b-125">-사이트</span><span class="sxs-lookup"><span data-stu-id="1f86b-125">-Site</span></span>
<span data-ttu-id="1f86b-126">설정 파일을 가져올 사이트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f86b-126">Specifies a site for which to get a settings file.</span></span>
<span data-ttu-id="1f86b-127">**사이트** 개체를 얻으려면 **AzureSiteRecoverySite** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f86b-127">To obtain a **Site** object, use the **Get-AzureSiteRecoverySite** cmdlet.</span></span>

```yaml
Type: ASRSite
Parameter Sets: ByObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f86b-128">-SiteId</span><span class="sxs-lookup"><span data-stu-id="1f86b-128">-SiteId</span></span>
<span data-ttu-id="1f86b-129">사이트의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f86b-129">Specifies the ID of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f86b-130">-SiteName</span><span class="sxs-lookup"><span data-stu-id="1f86b-130">-SiteName</span></span>
<span data-ttu-id="1f86b-131">사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f86b-131">Specifies the name of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f86b-132">-저장실</span><span class="sxs-lookup"><span data-stu-id="1f86b-132">-Vault</span></span>
<span data-ttu-id="1f86b-133">사이트의 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f86b-133">Specifies the vault for the site.</span></span>

```yaml
Type: ASRVault
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f86b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f86b-134">CommonParameters</span></span>
<span data-ttu-id="1f86b-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f86b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f86b-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f86b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f86b-137">입력</span><span class="sxs-lookup"><span data-stu-id="1f86b-137">INPUTS</span></span>

## <span data-ttu-id="1f86b-138">출력</span><span class="sxs-lookup"><span data-stu-id="1f86b-138">OUTPUTS</span></span>

## <span data-ttu-id="1f86b-139">상속자</span><span class="sxs-lookup"><span data-stu-id="1f86b-139">NOTES</span></span>

## <span data-ttu-id="1f86b-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f86b-140">RELATED LINKS</span></span>

[<span data-ttu-id="1f86b-141">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="1f86b-141">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)

[<span data-ttu-id="1f86b-142">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="1f86b-142">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="1f86b-143">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="1f86b-143">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="1f86b-144">가져오기-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1f86b-144">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)


