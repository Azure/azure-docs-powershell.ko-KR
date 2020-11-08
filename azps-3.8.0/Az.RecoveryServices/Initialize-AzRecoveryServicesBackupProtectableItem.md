---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/initialize-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 8bc2286cf6df736ee54390447e83f0337c031001
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044708"
---
# <span data-ttu-id="4feeb-101">Initialize-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4feeb-101">Initialize-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="4feeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4feeb-102">SYNOPSIS</span></span>
<span data-ttu-id="4feeb-103">이 명령은 주어진 컨테이너에서 지정 된 작업 부하 유형의 보호 되지 않은 항목에 대 한 검색을 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="4feeb-103">This command triggers the discovery of any unprotected items of the given workload type in the given container.</span></span> <span data-ttu-id="4feeb-104">DB 응용 프로그램이 자동으로 보호 되지 않는 경우이 명령을 사용 하 여 추가 될 때마다 새 db를 검색 하 고 계속 해 서 보호 하세요.</span><span class="sxs-lookup"><span data-stu-id="4feeb-104">If the DB application is not auto-protected use this command to discover new DBs whenever they are added and proceed to protect them.</span></span>

## <span data-ttu-id="4feeb-105">구문과</span><span class="sxs-lookup"><span data-stu-id="4feeb-105">SYNTAX</span></span>

```
Initialize-AzRecoveryServicesBackupProtectableItem [-Container] <ContainerBase> [-WorkloadType] <WorkloadType>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4feeb-106">설명은</span><span class="sxs-lookup"><span data-stu-id="4feeb-106">DESCRIPTION</span></span>
<span data-ttu-id="4feeb-107">컨테이너 내의 특정 작업 부하에 대 한 cmdlet 질문.</span><span class="sxs-lookup"><span data-stu-id="4feeb-107">the cmdlet enquires for specific workloads within a container.</span></span> <span data-ttu-id="4feeb-108">보호 가능한 항목을 만드는 작업을 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="4feeb-108">This triggers an operation which creates protectable items.</span></span>

## <span data-ttu-id="4feeb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4feeb-109">EXAMPLES</span></span>

### <span data-ttu-id="4feeb-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4feeb-110">Example 1</span></span>
```
PS C:\> Initialize-AzRecoveryServicesProtectableItem -Container $Container -WorkloadType "MSSQL"
```

<span data-ttu-id="4feeb-111">Cmdlet은 보호 가능한 새 항목에 대 한 검색 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4feeb-111">The cmdlet executes a discovery operation for new protectable items.</span></span>

## <span data-ttu-id="4feeb-112">변수</span><span class="sxs-lookup"><span data-stu-id="4feeb-112">PARAMETERS</span></span>

### <span data-ttu-id="4feeb-113">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="4feeb-113">-Container</span></span>
<span data-ttu-id="4feeb-114">항목이 있는 컨테이너</span><span class="sxs-lookup"><span data-stu-id="4feeb-114">Container where the item resides</span></span>

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

### <span data-ttu-id="4feeb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4feeb-115">-DefaultProfile</span></span>
<span data-ttu-id="4feeb-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4feeb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4feeb-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4feeb-117">-PassThru</span></span>
<span data-ttu-id="4feeb-118">삭제할 컨테이너를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4feeb-118">Return the container to be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4feeb-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4feeb-119">-VaultId</span></span>
<span data-ttu-id="4feeb-120">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4feeb-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4feeb-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="4feeb-121">-WorkloadType</span></span>
<span data-ttu-id="4feeb-122">리소스의 작업 부하 유형 (예: Add-azurevm, WindowsServer, AzureFiles, MSSQL)입니다.</span><span class="sxs-lookup"><span data-stu-id="4feeb-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

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

### <span data-ttu-id="4feeb-123">-확인</span><span class="sxs-lookup"><span data-stu-id="4feeb-123">-Confirm</span></span>
<span data-ttu-id="4feeb-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4feeb-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4feeb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4feeb-125">-WhatIf</span></span>
<span data-ttu-id="4feeb-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4feeb-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4feeb-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4feeb-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4feeb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4feeb-128">CommonParameters</span></span>
<span data-ttu-id="4feeb-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4feeb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4feeb-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4feeb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4feeb-131">입력</span><span class="sxs-lookup"><span data-stu-id="4feeb-131">INPUTS</span></span>

### <span data-ttu-id="4feeb-132">ContainerBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="4feeb-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="4feeb-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4feeb-133">System.String</span></span>

## <span data-ttu-id="4feeb-134">출력</span><span class="sxs-lookup"><span data-stu-id="4feeb-134">OUTPUTS</span></span>

### <span data-ttu-id="4feeb-135">Microsoft Azure.. i g i..</span><span class="sxs-lookup"><span data-stu-id="4feeb-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="4feeb-136">상속자</span><span class="sxs-lookup"><span data-stu-id="4feeb-136">NOTES</span></span>

## <span data-ttu-id="4feeb-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4feeb-137">RELATED LINKS</span></span>
