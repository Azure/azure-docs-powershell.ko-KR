---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 0dac27b7e17a9336db198906cdfb60fb15738795
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526711"
---
# <span data-ttu-id="bfd6c-101">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="bfd6c-101">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="bfd6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfd6c-102">SYNOPSIS</span></span>
<span data-ttu-id="bfd6c-103">SCDPM 및 Azure 백업 관리 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-103">Gets SCDPM and Azure Backup management servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfd6c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bfd6c-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupManagementServer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bfd6c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bfd6c-105">DESCRIPTION</span></span>
<span data-ttu-id="bfd6c-106">**AzureRmRecoveryServicesBackupManagementServer** cmdlet은 자격 증명 모음에 등록 된 백업 관리 서버의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-106">The **Get-AzureRmRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>

<span data-ttu-id="bfd6c-107">백업 관리 서버에는 SCDPM (System Center Data Protection Manager) 및 Azure Backup 관리 서버가 두 가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="bfd6c-108">백업 관리 서버는 개별적으로 설치 되어 백업 오케스트레이션을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>

<span data-ttu-id="bfd6c-109">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="bfd6c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="bfd6c-110">EXAMPLES</span></span>

### <span data-ttu-id="bfd6c-111">예제 1: 모든 백업 관리 서버 가져오기</span><span class="sxs-lookup"><span data-stu-id="bfd6c-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupManagementServer
```

<span data-ttu-id="bfd6c-112">이 명령은 자격 증명 모음에 등록 된 모든 백업 관리 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="bfd6c-113">변수</span><span class="sxs-lookup"><span data-stu-id="bfd6c-113">PARAMETERS</span></span>

### <span data-ttu-id="bfd6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfd6c-114">-DefaultProfile</span></span>
<span data-ttu-id="bfd6c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfd6c-116">-이름</span><span class="sxs-lookup"><span data-stu-id="bfd6c-116">-Name</span></span>
<span data-ttu-id="bfd6c-117">가져올 백업 관리 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-117">Specifies the name of the Backup management server to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfd6c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfd6c-118">CommonParameters</span></span>
<span data-ttu-id="bfd6c-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfd6c-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfd6c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfd6c-121">입력</span><span class="sxs-lookup"><span data-stu-id="bfd6c-121">INPUTS</span></span>

### <span data-ttu-id="bfd6c-122">않아야</span><span class="sxs-lookup"><span data-stu-id="bfd6c-122">None</span></span>
<span data-ttu-id="bfd6c-123">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bfd6c-124">출력</span><span class="sxs-lookup"><span data-stu-id="bfd6c-124">OUTPUTS</span></span>

### <span data-ttu-id="bfd6c-125">BackupEngineBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-125">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

### <span data-ttu-id="bfd6c-126">System.webserver. IList ' 1 [Microsoft Azure. e. BackupEngineBase]을 (를)</span><span class="sxs-lookup"><span data-stu-id="bfd6c-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase]</span></span>

## <span data-ttu-id="bfd6c-127">상속자</span><span class="sxs-lookup"><span data-stu-id="bfd6c-127">NOTES</span></span>

## <span data-ttu-id="bfd6c-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bfd6c-128">RELATED LINKS</span></span>

[<span data-ttu-id="bfd6c-129">등록 취소-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="bfd6c-129">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzureRmRecoveryServicesBackupManagementServer.md)


