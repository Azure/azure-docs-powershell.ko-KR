---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 09d27926f489feea397c98a217840bb973e002ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034347"
---
# <span data-ttu-id="9ef57-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="9ef57-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="9ef57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ef57-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef57-103">SCDPM 및 Azure 백업 관리 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ef57-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="9ef57-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ef57-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ef57-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9ef57-105">DESCRIPTION</span></span>
<span data-ttu-id="9ef57-106">**AzRecoveryServicesBackupManagementServer** cmdlet은 자격 증명 모음에 등록 된 백업 관리 서버의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ef57-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="9ef57-107">백업 관리 서버에는 SCDPM (System Center Data Protection Manager) 및 Azure Backup 관리 서버가 두 가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ef57-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="9ef57-108">백업 관리 서버는 개별적으로 설치 되어 백업 오케스트레이션을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef57-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="9ef57-109">현재 cmdlet을 사용 하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef57-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="9ef57-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9ef57-110">EXAMPLES</span></span>

### <span data-ttu-id="9ef57-111">예제 1: 모든 백업 관리 서버 가져오기</span><span class="sxs-lookup"><span data-stu-id="9ef57-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="9ef57-112">이 명령은 자격 증명 모음에 등록 된 모든 백업 관리 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ef57-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="9ef57-113">변수</span><span class="sxs-lookup"><span data-stu-id="9ef57-113">PARAMETERS</span></span>

### <span data-ttu-id="9ef57-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef57-114">-DefaultProfile</span></span>
<span data-ttu-id="9ef57-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ef57-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ef57-116">-이름</span><span class="sxs-lookup"><span data-stu-id="9ef57-116">-Name</span></span>
<span data-ttu-id="9ef57-117">가져올 백업 관리 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef57-117">Specifies the name of the Backup management server to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef57-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9ef57-118">-VaultId</span></span>
<span data-ttu-id="9ef57-119">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9ef57-119">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ef57-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef57-120">CommonParameters</span></span>
<span data-ttu-id="9ef57-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef57-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef57-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ef57-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef57-123">입력</span><span class="sxs-lookup"><span data-stu-id="9ef57-123">INPUTS</span></span>

### <span data-ttu-id="9ef57-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9ef57-124">System.String</span></span>

## <span data-ttu-id="9ef57-125">출력</span><span class="sxs-lookup"><span data-stu-id="9ef57-125">OUTPUTS</span></span>

### <span data-ttu-id="9ef57-126">BackupEngineBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="9ef57-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="9ef57-127">상속자</span><span class="sxs-lookup"><span data-stu-id="9ef57-127">NOTES</span></span>

## <span data-ttu-id="9ef57-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ef57-128">RELATED LINKS</span></span>

[<span data-ttu-id="9ef57-129">등록 취소-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="9ef57-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)


