---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9882F1A5-6FFB-4DAF-8ED5-B14596BC939D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvaultcredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
ms.openlocfilehash: 6ee9e3062108049e517dbea09573af7905dd54d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703473"
---
# <span data-ttu-id="734ea-101">Get-AzureRmBackupVaultCredentials</span><span class="sxs-lookup"><span data-stu-id="734ea-101">Get-AzureRmBackupVaultCredentials</span></span>

## <span data-ttu-id="734ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="734ea-102">SYNOPSIS</span></span>
<span data-ttu-id="734ea-103">백업 자격 증명 모음의 자격 증명 모음 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="734ea-103">Downloads the vault credentials file for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="734ea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="734ea-104">SYNTAX</span></span>

```
Get-AzureRmBackupVaultCredentials [-TargetLocation] <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="734ea-105">설명은</span><span class="sxs-lookup"><span data-stu-id="734ea-105">DESCRIPTION</span></span>
<span data-ttu-id="734ea-106">**AzureRmBackupVaultCredentials** Cmdlet은 Azure Backup 자격 증명 모음에 대 한 자격 증명 모음 인증서 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="734ea-106">The **Get-AzureRmBackupVaultCredentials** cmdlet downloads the vault credentials file for an Azure Backup vault.</span></span>
<span data-ttu-id="734ea-107">백업은 자격 증명 모음 자격 증명 파일을 사용 하 여 서버를 Azure Backup 자격 증명 모음에 연결 하 고 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="734ea-107">Backup uses a vault credential file to connect a server to the Azure Backup vault and register it.</span></span>
<span data-ttu-id="734ea-108">백업이 자격 증명 모음에 백업 데이터를 보낼 수 있으려면 먼저 서버를 등록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="734ea-108">You must register a server before Backup can send backup data to the vault.</span></span>

## <span data-ttu-id="734ea-109">예제의</span><span class="sxs-lookup"><span data-stu-id="734ea-109">EXAMPLES</span></span>

## <span data-ttu-id="734ea-110">변수</span><span class="sxs-lookup"><span data-stu-id="734ea-110">PARAMETERS</span></span>

### <span data-ttu-id="734ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="734ea-111">-DefaultProfile</span></span>
<span data-ttu-id="734ea-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="734ea-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="734ea-113">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="734ea-113">-TargetLocation</span></span>
<span data-ttu-id="734ea-114">이 cmdlet이 저장실 자격 증명 파일을 저장 하는 대상 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="734ea-114">Specifies the destination path where this cmdlet stores the vault credentials file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="734ea-115">-저장실</span><span class="sxs-lookup"><span data-stu-id="734ea-115">-Vault</span></span>
<span data-ttu-id="734ea-116">이 cmdlet이 저장실 자격 증명 파일을 가져오는 백업 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="734ea-116">Specifies the Backup vault for which this cmdlet gets a vault credential file.</span></span>
<span data-ttu-id="734ea-117">**AzureRmBackupVault** 개체를 가져오려면 Get-AzureRmBackupVault cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="734ea-117">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="734ea-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="734ea-118">CommonParameters</span></span>
<span data-ttu-id="734ea-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="734ea-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="734ea-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="734ea-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="734ea-121">입력</span><span class="sxs-lookup"><span data-stu-id="734ea-121">INPUTS</span></span>

### <span data-ttu-id="734ea-122">AzureRMBackupVault를 통한 명령.</span><span class="sxs-lookup"><span data-stu-id="734ea-122">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="734ea-123">매개 변수: 자격 증명 모음 (ByValue)</span><span class="sxs-lookup"><span data-stu-id="734ea-123">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="734ea-124">출력</span><span class="sxs-lookup"><span data-stu-id="734ea-124">OUTPUTS</span></span>

### <span data-ttu-id="734ea-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="734ea-125">System.String</span></span>
<span data-ttu-id="734ea-126">이 cmdlet은 자격 증명 모음 인증서 파일의 이름을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="734ea-126">This cmdlet returns the name of the vault credential file.</span></span>

## <span data-ttu-id="734ea-127">상속자</span><span class="sxs-lookup"><span data-stu-id="734ea-127">NOTES</span></span>

## <span data-ttu-id="734ea-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="734ea-128">RELATED LINKS</span></span>

[<span data-ttu-id="734ea-129">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="734ea-129">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


