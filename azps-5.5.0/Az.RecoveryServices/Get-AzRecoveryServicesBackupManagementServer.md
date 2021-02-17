---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 09d27926f489feea397c98a217840bb973e002ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189329"
---
# <span data-ttu-id="7876e-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="7876e-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="7876e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7876e-102">SYNOPSIS</span></span>
<span data-ttu-id="7876e-103">SCDPM 및 Azure Backup 관리 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7876e-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="7876e-104">구문</span><span class="sxs-lookup"><span data-stu-id="7876e-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7876e-105">설명</span><span class="sxs-lookup"><span data-stu-id="7876e-105">DESCRIPTION</span></span>
<span data-ttu-id="7876e-106">**Get-AzRecoveryServicesBackupManagementServer** cmdlet은 자격 증명 모음에 등록된 Backup 관리 서버 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7876e-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="7876e-107">Backup 관리 서버에는 SCDPM(System Center Data Protection Manager) 및 Azure Backup 관리 서버의 두 가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7876e-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="7876e-108">Backup 관리 서버는 Backup 오케스트레이션을 관리하기 위해 별도로 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="7876e-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="7876e-109">현재 cmdlet을 사용하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용하여 자격 증명 모음 컨텍스트를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7876e-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="7876e-110">예제</span><span class="sxs-lookup"><span data-stu-id="7876e-110">EXAMPLES</span></span>

### <span data-ttu-id="7876e-111">예제 1: 모든 Backup 관리 서버 얻기</span><span class="sxs-lookup"><span data-stu-id="7876e-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="7876e-112">이 명령은 자격 증명 모음에 등록된 모든 Backup 관리 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7876e-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="7876e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7876e-113">PARAMETERS</span></span>

### <span data-ttu-id="7876e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7876e-114">-DefaultProfile</span></span>
<span data-ttu-id="7876e-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7876e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7876e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7876e-116">-Name</span></span>
<span data-ttu-id="7876e-117">얻을 Backup 관리 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7876e-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="7876e-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7876e-118">-VaultId</span></span>
<span data-ttu-id="7876e-119">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7876e-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7876e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7876e-120">CommonParameters</span></span>
<span data-ttu-id="7876e-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7876e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7876e-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7876e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7876e-123">입력</span><span class="sxs-lookup"><span data-stu-id="7876e-123">INPUTS</span></span>

### <span data-ttu-id="7876e-124">System.String</span><span class="sxs-lookup"><span data-stu-id="7876e-124">System.String</span></span>

## <span data-ttu-id="7876e-125">출력</span><span class="sxs-lookup"><span data-stu-id="7876e-125">OUTPUTS</span></span>

### <span data-ttu-id="7876e-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="7876e-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="7876e-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7876e-127">NOTES</span></span>

## <span data-ttu-id="7876e-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7876e-128">RELATED LINKS</span></span>

[<span data-ttu-id="7876e-129">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="7876e-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)


