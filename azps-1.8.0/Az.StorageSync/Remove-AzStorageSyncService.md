---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: 5116ead7111902b1009517ff42ff6594ac87d8c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698475"
---
# <span data-ttu-id="ca696-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ca696-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="ca696-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca696-102">SYNOPSIS</span></span>
<span data-ttu-id="ca696-103">이 명령은 지정 된 저장소 동기화 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca696-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="ca696-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ca696-104">SYNTAX</span></span>

### <span data-ttu-id="ca696-105">InputObjectParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ca696-105">InputObjectParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca696-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca696-106">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca696-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca696-107">StringParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca696-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ca696-108">DESCRIPTION</span></span>
<span data-ttu-id="ca696-109">이 명령은 지정 된 저장소 동기화 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca696-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="ca696-110">저장소 동기화 서비스는 포함 된 모든 동기화 그룹 및 등록 된 서버가 먼저 삭제 된 경우에만 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca696-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="ca696-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ca696-111">EXAMPLES</span></span>

### <span data-ttu-id="ca696-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ca696-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="ca696-113">이 명령은 저장소 동기화 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca696-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="ca696-114">변수</span><span class="sxs-lookup"><span data-stu-id="ca696-114">PARAMETERS</span></span>

### <span data-ttu-id="ca696-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca696-115">-AsJob</span></span>
<span data-ttu-id="ca696-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ca696-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca696-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca696-117">-DefaultProfile</span></span>
<span data-ttu-id="ca696-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca696-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca696-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ca696-119">-Force</span></span>
<span data-ttu-id="ca696-120">이 명령에 대 한 확인을 건너뛰기 위해-Force를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca696-120">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca696-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca696-121">-InputObject</span></span>
<span data-ttu-id="ca696-122">일반적으로 파이프라인을 통해 전달 되는 Storages<c13> Cservice 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ca696-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca696-123">-이름</span><span class="sxs-lookup"><span data-stu-id="ca696-123">-Name</span></span>
<span data-ttu-id="ca696-124">Storages<c13> Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca696-124">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca696-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca696-125">-PassThru</span></span>
<span data-ttu-id="ca696-126">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="ca696-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ca696-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca696-127">-ResourceGroupName</span></span>
<span data-ttu-id="ca696-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca696-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca696-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca696-129">-ResourceId</span></span>
<span data-ttu-id="ca696-130">Storages<c13> Cservice 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="ca696-130">StorageSyncService Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca696-131">-확인</span><span class="sxs-lookup"><span data-stu-id="ca696-131">-Confirm</span></span>
<span data-ttu-id="ca696-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca696-132">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca696-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca696-133">-WhatIf</span></span>
<span data-ttu-id="ca696-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ca696-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca696-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca696-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca696-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca696-136">CommonParameters</span></span>
<span data-ttu-id="ca696-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca696-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca696-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca696-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca696-139">입력</span><span class="sxs-lookup"><span data-stu-id="ca696-139">INPUTS</span></span>

### <span data-ttu-id="ca696-140">StorageSync. Psstorages Cservice</span><span class="sxs-lookup"><span data-stu-id="ca696-140">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="ca696-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ca696-141">System.String</span></span>

### <span data-ttu-id="ca696-142">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ca696-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ca696-143">출력</span><span class="sxs-lookup"><span data-stu-id="ca696-143">OUTPUTS</span></span>

### <span data-ttu-id="ca696-144">System. 개체</span><span class="sxs-lookup"><span data-stu-id="ca696-144">System.Object</span></span>
## <span data-ttu-id="ca696-145">상속자</span><span class="sxs-lookup"><span data-stu-id="ca696-145">NOTES</span></span>

## <span data-ttu-id="ca696-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca696-146">RELATED LINKS</span></span>
