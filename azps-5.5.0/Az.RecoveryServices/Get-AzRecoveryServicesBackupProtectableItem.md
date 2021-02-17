---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 580f5fd7dc85857bff7257847806bb15dc646ad3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191377"
---
# <span data-ttu-id="c6f33-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c6f33-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="c6f33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6f33-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f33-103">이 명령은 특정 컨테이너 내에서 또는 등록된 모든 컨테이너에서 보호 가능한 모든 항목을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f33-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="c6f33-104">애플리케이션의 계층 구조의 모든 요소로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6f33-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="c6f33-105">인스턴스, AvailabilityGroup 등, DB 및 해당 상위 계층 엔터티를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f33-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="c6f33-106">구문</span><span class="sxs-lookup"><span data-stu-id="c6f33-106">SYNTAX</span></span>

### <span data-ttu-id="c6f33-107">NoFilterParamSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c6f33-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6f33-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="c6f33-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6f33-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="c6f33-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6f33-110">설명</span><span class="sxs-lookup"><span data-stu-id="c6f33-110">DESCRIPTION</span></span>
<span data-ttu-id="c6f33-111">**Get-AzRecoveryServicesBackupProtectableItem** cmdlet은 컨테이너의 보호 가능한 항목 목록과 항목의 보호 상태를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f33-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the list of protectable items in a container and the protection status of the items.</span></span>
<span data-ttu-id="c6f33-112">Azure Recovery Services 자격 증명 모음에 등록된 컨테이너에는 보호할 수 있는 하나 이상의 항목이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6f33-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="c6f33-113">예제</span><span class="sxs-lookup"><span data-stu-id="c6f33-113">EXAMPLES</span></span>

### <span data-ttu-id="c6f33-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="c6f33-114">Example 1</span></span>
```
PS C:\> $Vault = Get-AzRecoveryServicesVault -Name "MyRecoveryVault"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer -Status Registered -VaultId $Vault.Id
PS C:\> $Item = Get-AzRecoveryServicesBackupProtectableItem -Container $Container -ItemType "SQLInstance" -WorkloadType "MSSQL" -VaultId $Vault.ID
```

<span data-ttu-id="c6f33-115">첫 번째 명령은 MSSQL 형식의 컨테이너를 인용한 다음, $Container 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f33-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="c6f33-116">두 번째 명령은 백업 보호 가능한 항목을 $Container 백업 변수에 $Item 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f33-116">The second command gets the Backup protectable item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="c6f33-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6f33-117">PARAMETERS</span></span>

### <span data-ttu-id="c6f33-118">-Container</span><span class="sxs-lookup"><span data-stu-id="c6f33-118">-Container</span></span>
<span data-ttu-id="c6f33-119">항목이 있는 컨테이너</span><span class="sxs-lookup"><span data-stu-id="c6f33-119">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f33-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f33-120">-DefaultProfile</span></span>
<span data-ttu-id="c6f33-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f33-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6f33-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="c6f33-122">-ItemType</span></span>
<span data-ttu-id="c6f33-123">보호 가능한 항목의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f33-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="c6f33-124">해당 값: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span><span class="sxs-lookup"><span data-stu-id="c6f33-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemType
Parameter Sets: FilterParamSet, IdParamSet
Aliases:
Accepted values: SQLDataBase, SQLInstance, SQLAvailabilityGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f33-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c6f33-125">-Name</span></span>
<span data-ttu-id="c6f33-126">데이터베이스, 인스턴스 또는 AvailabilityGroup의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f33-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f33-127">-ParentID</span><span class="sxs-lookup"><span data-stu-id="c6f33-127">-ParentID</span></span>
<span data-ttu-id="c6f33-128">인스턴스 또는 ARM ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f33-128">Specified the ARM ID of an Instance or AG.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f33-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c6f33-129">-ServerName</span></span>
<span data-ttu-id="c6f33-130">항목이 속한 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f33-130">Specifies the name of the server to which the item belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f33-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c6f33-131">-VaultId</span></span>
<span data-ttu-id="c6f33-132">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f33-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c6f33-133">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="c6f33-133">-WorkloadType</span></span>
<span data-ttu-id="c6f33-134">리소스의 워크로드 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f33-134">Workload type of the resource.</span></span> <span data-ttu-id="c6f33-135">현재 지원되는 값은 AzureVM, WindowsServer, AzureFiles, MSSQL입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f33-135">The current supported values are  AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:
Accepted values: AzureVM, WindowsServer, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f33-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f33-136">CommonParameters</span></span>
<span data-ttu-id="c6f33-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f33-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f33-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c6f33-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f33-139">입력</span><span class="sxs-lookup"><span data-stu-id="c6f33-139">INPUTS</span></span>

### <span data-ttu-id="c6f33-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="c6f33-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="c6f33-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c6f33-141">System.String</span></span>

## <span data-ttu-id="c6f33-142">출력</span><span class="sxs-lookup"><span data-stu-id="c6f33-142">OUTPUTS</span></span>

### <span data-ttu-id="c6f33-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="c6f33-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="c6f33-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c6f33-144">NOTES</span></span>

## <span data-ttu-id="c6f33-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6f33-145">RELATED LINKS</span></span>
