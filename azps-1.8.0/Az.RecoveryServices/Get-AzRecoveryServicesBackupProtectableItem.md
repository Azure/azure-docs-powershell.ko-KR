---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 03e990f36c8846ad1055d5d2f8873ead18536128
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699699"
---
# <span data-ttu-id="41881-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="41881-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="41881-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41881-102">SYNOPSIS</span></span>
<span data-ttu-id="41881-103">이 명령은 특정 컨테이너 내에서 또는 등록 된 모든 컨테이너에서 보호 가능한 모든 항목을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="41881-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="41881-104">응용 프로그램 계층 구조의 모든 요소로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="41881-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="41881-105">인스턴스, AvailabilityGroup 등의 상위 계층 엔터티를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="41881-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="41881-106">구문과</span><span class="sxs-lookup"><span data-stu-id="41881-106">SYNTAX</span></span>

### <span data-ttu-id="41881-107">NoFilterParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="41881-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41881-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="41881-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41881-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="41881-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41881-110">설명은</span><span class="sxs-lookup"><span data-stu-id="41881-110">DESCRIPTION</span></span>
<span data-ttu-id="41881-111">**AzRecoveryServicesBackupProtectableItem** cmdlet은 컨테이너의 보호 가능한 항목 또는 Azure Backup의 값과 항목의 보호 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="41881-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the protectable items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="41881-112">Azure Recovery Services 자격 증명 모음에 등록 된 컨테이너에는 보호할 수 있는 항목이 하나 이상 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41881-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="41881-113">예제의</span><span class="sxs-lookup"><span data-stu-id="41881-113">EXAMPLES</span></span>

### <span data-ttu-id="41881-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="41881-114">Example 1</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType MSSQL -Status Registered
PS C:\> $Item = Get-AzRecoveryServicesProtectableItem -Container $Container -ItemType "SQLDatabase" -VaultId $vault.ID
```

<span data-ttu-id="41881-115">첫 번째 명령은 MSSQL 형식의 컨테이너를 가져온 다음 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="41881-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="41881-116">두 번째 명령은 $Container에서 백업 항목을 가져온 다음 $Item 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="41881-116">The second command gets the Backup item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="41881-117">변수</span><span class="sxs-lookup"><span data-stu-id="41881-117">PARAMETERS</span></span>

### <span data-ttu-id="41881-118">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="41881-118">-Container</span></span>
<span data-ttu-id="41881-119">항목이 있는 컨테이너</span><span class="sxs-lookup"><span data-stu-id="41881-119">Container where the item resides</span></span>

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

### <span data-ttu-id="41881-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41881-120">-DefaultProfile</span></span>
<span data-ttu-id="41881-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41881-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41881-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="41881-122">-ItemType</span></span>
<span data-ttu-id="41881-123">보호 가능한 항목의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41881-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="41881-124">해당 되는 값: (SQLDataBase, SQLInstance, SQLAvailabilityGroup)</span><span class="sxs-lookup"><span data-stu-id="41881-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

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

### <span data-ttu-id="41881-125">-이름</span><span class="sxs-lookup"><span data-stu-id="41881-125">-Name</span></span>
<span data-ttu-id="41881-126">데이터베이스, 인스턴스 또는 AvailabilityGroup의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41881-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

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

### <span data-ttu-id="41881-127">-ParentID</span><span class="sxs-lookup"><span data-stu-id="41881-127">-ParentID</span></span>
<span data-ttu-id="41881-128">인스턴스 또는 AG의 ARM ID를 지정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="41881-128">Specified the ARM ID of an Instance or AG.</span></span>

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

### <span data-ttu-id="41881-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="41881-129">-ServerName</span></span>
<span data-ttu-id="41881-130">항목이 속한 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41881-130">Specifies the name of the server to which the item belongs.</span></span>

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

### <span data-ttu-id="41881-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="41881-131">-VaultId</span></span>
<span data-ttu-id="41881-132">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="41881-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="41881-133">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="41881-133">-WorkloadType</span></span>
<span data-ttu-id="41881-134">리소스의 작업 부하 유형 (예: Add-azurevm, WindowsServer, AzureFiles, MSSQL)입니다.</span><span class="sxs-lookup"><span data-stu-id="41881-134">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41881-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41881-135">CommonParameters</span></span>
<span data-ttu-id="41881-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41881-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41881-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41881-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41881-138">입력</span><span class="sxs-lookup"><span data-stu-id="41881-138">INPUTS</span></span>

### <span data-ttu-id="41881-139">ContainerBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="41881-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="41881-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="41881-140">System.String</span></span>

## <span data-ttu-id="41881-141">출력</span><span class="sxs-lookup"><span data-stu-id="41881-141">OUTPUTS</span></span>

### <span data-ttu-id="41881-142">ProtectableItemBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="41881-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="41881-143">상속자</span><span class="sxs-lookup"><span data-stu-id="41881-143">NOTES</span></span>

## <span data-ttu-id="41881-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41881-144">RELATED LINKS</span></span>