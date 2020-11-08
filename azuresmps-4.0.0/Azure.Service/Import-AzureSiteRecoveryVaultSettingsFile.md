---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5875D72D-B8DB-4F72-BF5C-242D40A13DE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5dc0762021db2545b73a9ba7b9d7c53d435ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046260"
---
# <span data-ttu-id="fdeb0-101">Import-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="fdeb0-101">Import-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="fdeb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdeb0-102">SYNOPSIS</span></span>
<span data-ttu-id="fdeb0-103">사이트 복구 자격 증명 모음 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fdeb0-103">Imports a Site Recovery vault settings file.</span></span>

## <span data-ttu-id="fdeb0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fdeb0-104">SYNTAX</span></span>

```
Import-AzureSiteRecoveryVaultSettingsFile -Path <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fdeb0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fdeb0-105">DESCRIPTION</span></span>
<span data-ttu-id="fdeb0-106">**AzureSiteRecoveryVaultSettingsFile** Cmdlet은 Azure Site recovery 자격 증명 모음 설정 파일을 가져와 현재 세션의 후속 사이트 복구 작업에 대 한 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdeb0-106">The **Import-AzureSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="fdeb0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fdeb0-107">EXAMPLES</span></span>

### <span data-ttu-id="fdeb0-108">예제 1: 자격 증명 모음 설정 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="fdeb0-108">Example 1: Import a vault settings file</span></span>
```
PS C:\> Import-AzureSiteRecoveryVaultSettingsFile -Path "C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials"
VERBOSE: Vault Settings File path: C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials

ResourceName                                                CloudServiceName
------------                                                ----------------
Contosovault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="fdeb0-109">이 명령은 지정 된 경로에서 보관소 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fdeb0-109">This command imports the vault settings file at the specified path.</span></span>

## <span data-ttu-id="fdeb0-110">변수</span><span class="sxs-lookup"><span data-stu-id="fdeb0-110">PARAMETERS</span></span>

### <span data-ttu-id="fdeb0-111">-Path</span><span class="sxs-lookup"><span data-stu-id="fdeb0-111">-Path</span></span>
<span data-ttu-id="fdeb0-112">사이트 복구 자격 증명 모음 설정 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdeb0-112">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="fdeb0-113">이 파일은 사이트 복구 자격 증명 모음 포털에서 다운로드 하 여 로컬에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdeb0-113">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdeb0-114">-프로필</span><span class="sxs-lookup"><span data-stu-id="fdeb0-114">-Profile</span></span>
<span data-ttu-id="fdeb0-115">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdeb0-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fdeb0-116">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="fdeb0-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fdeb0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdeb0-117">CommonParameters</span></span>
<span data-ttu-id="fdeb0-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdeb0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdeb0-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdeb0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdeb0-120">입력</span><span class="sxs-lookup"><span data-stu-id="fdeb0-120">INPUTS</span></span>

## <span data-ttu-id="fdeb0-121">출력</span><span class="sxs-lookup"><span data-stu-id="fdeb0-121">OUTPUTS</span></span>

## <span data-ttu-id="fdeb0-122">상속자</span><span class="sxs-lookup"><span data-stu-id="fdeb0-122">NOTES</span></span>

## <span data-ttu-id="fdeb0-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fdeb0-123">RELATED LINKS</span></span>

[<span data-ttu-id="fdeb0-124">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="fdeb0-124">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="fdeb0-125">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="fdeb0-125">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)


