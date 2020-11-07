---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/initialize-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 0fd0473cccdf8fbef3d3bab941ab6b3ce7813a63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699677"
---
# <span data-ttu-id="d7433-101">Initialize-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d7433-101">Initialize-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="d7433-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7433-102">SYNOPSIS</span></span>
<span data-ttu-id="d7433-103">이 명령은 주어진 컨테이너에서 지정 된 작업 부하 유형의 보호 되지 않은 항목에 대 한 검색을 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="d7433-103">This command triggers the discovery of any unprotected items of the given workload type in the given container.</span></span> <span data-ttu-id="d7433-104">DB 응용 프로그램이 자동으로 보호 되지 않는 경우이 명령을 사용 하 여 추가 될 때마다 새 db를 검색 하 고 계속 해 서 보호 하세요.</span><span class="sxs-lookup"><span data-stu-id="d7433-104">If the DB application is not auto-protected use this command to discover new DBs whenever they are added and proceed to protect them.</span></span>

## <span data-ttu-id="d7433-105">구문과</span><span class="sxs-lookup"><span data-stu-id="d7433-105">SYNTAX</span></span>

```
Initialize-AzRecoveryServicesBackupProtectableItem [-Container] <ContainerBase> [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7433-106">설명은</span><span class="sxs-lookup"><span data-stu-id="d7433-106">DESCRIPTION</span></span>
<span data-ttu-id="d7433-107">컨테이너 내의 특정 작업 부하에 대 한 cmdlet 질문.</span><span class="sxs-lookup"><span data-stu-id="d7433-107">the cmdlet enquires for specific workloads within a container.</span></span> <span data-ttu-id="d7433-108">보호 가능한 항목을 만드는 작업을 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="d7433-108">This triggers an operation which creates protectable items.</span></span>

## <span data-ttu-id="d7433-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d7433-109">EXAMPLES</span></span>

### <span data-ttu-id="d7433-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d7433-110">Example 1</span></span>
```
PS C:\> Initialize-AzRecoveryServicesProtectableItem -Container $Container –WorkloadType “MSSQL”
```

<span data-ttu-id="d7433-111">Cmdlet은 보호 가능한 새 항목에 대 한 검색 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7433-111">The cmdlet executes a discovery operation for new protectable items.</span></span>

## <span data-ttu-id="d7433-112">변수</span><span class="sxs-lookup"><span data-stu-id="d7433-112">PARAMETERS</span></span>

### <span data-ttu-id="d7433-113">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="d7433-113">-Container</span></span>
<span data-ttu-id="d7433-114">항목이 있는 컨테이너</span><span class="sxs-lookup"><span data-stu-id="d7433-114">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7433-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7433-115">-DefaultProfile</span></span>
<span data-ttu-id="d7433-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7433-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7433-117">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d7433-117">-VaultId</span></span>
<span data-ttu-id="d7433-118">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d7433-118">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d7433-119">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="d7433-119">-WorkloadType</span></span>
<span data-ttu-id="d7433-120">리소스의 작업 부하 유형 (예: Add-azurevm, WindowsServer, AzureFiles, MSSQL)입니다.</span><span class="sxs-lookup"><span data-stu-id="d7433-120">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7433-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7433-121">CommonParameters</span></span>
<span data-ttu-id="d7433-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7433-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7433-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7433-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7433-124">입력</span><span class="sxs-lookup"><span data-stu-id="d7433-124">INPUTS</span></span>

### <span data-ttu-id="d7433-125">ContainerBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="d7433-125">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="d7433-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d7433-126">System.String</span></span>

## <span data-ttu-id="d7433-127">출력</span><span class="sxs-lookup"><span data-stu-id="d7433-127">OUTPUTS</span></span>

### <span data-ttu-id="d7433-128">Microsoft Azure.. i g i..</span><span class="sxs-lookup"><span data-stu-id="d7433-128">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="d7433-129">상속자</span><span class="sxs-lookup"><span data-stu-id="d7433-129">NOTES</span></span>

## <span data-ttu-id="d7433-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7433-130">RELATED LINKS</span></span>