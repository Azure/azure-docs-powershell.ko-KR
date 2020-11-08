---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 04ad7f188a2280dcdf84e8b5c1f45e20edf4d07b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211622"
---
# <span data-ttu-id="e0131-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="e0131-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="e0131-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0131-102">SYNOPSIS</span></span>
<span data-ttu-id="e0131-103">대상 볼륨에서 복제 연결을 제거/삭제 하 고 원본 복제에 릴리스를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="e0131-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="e0131-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e0131-104">SYNTAX</span></span>

### <span data-ttu-id="e0131-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e0131-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0131-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0131-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0131-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0131-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0131-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e0131-108">DESCRIPTION</span></span>
<span data-ttu-id="e0131-109">대상 볼륨에서 복제 연결을 제거/삭제 하 고 원본 복제에 릴리스를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="e0131-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="e0131-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e0131-110">EXAMPLES</span></span>

### <span data-ttu-id="e0131-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e0131-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="e0131-112">이 명령은 "MyDestinationAnfVolume" 볼륨에서 ANF 복제 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0131-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="e0131-113">변수</span><span class="sxs-lookup"><span data-stu-id="e0131-113">PARAMETERS</span></span>

### <span data-ttu-id="e0131-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e0131-114">-AccountName</span></span>
<span data-ttu-id="e0131-115">복제 볼륨의 ANF 계정 이름</span><span class="sxs-lookup"><span data-stu-id="e0131-115">The name of the ANF account of the replication volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0131-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0131-116">-DefaultProfile</span></span>
<span data-ttu-id="e0131-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0131-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0131-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0131-118">-InputObject</span></span>
<span data-ttu-id="e0131-119">제거할 복제를 포함 하는 ANF 대상 볼륨</span><span class="sxs-lookup"><span data-stu-id="e0131-119">The ANF destination volume with the replication to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0131-120">-이름</span><span class="sxs-lookup"><span data-stu-id="e0131-120">-Name</span></span>
<span data-ttu-id="e0131-121">ANF 복제 대상 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0131-121">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0131-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0131-122">-PassThru</span></span>
<span data-ttu-id="e0131-123">지정 된 ANF 복제가 성공적으로 제거 되었는지 여부 반환</span><span class="sxs-lookup"><span data-stu-id="e0131-123">Return whether the specified ANF replication was successfully removed</span></span>

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

### <span data-ttu-id="e0131-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="e0131-124">-PoolName</span></span>
<span data-ttu-id="e0131-125">복제 볼륨의 ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0131-125">The name of the ANF pool of the replication volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0131-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0131-126">-ResourceGroupName</span></span>
<span data-ttu-id="e0131-127">ANF 복제 대상 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="e0131-127">The resource group of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0131-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0131-128">-ResourceId</span></span>
<span data-ttu-id="e0131-129">ANF 복제 대상 볼륨의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="e0131-129">The resource id of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0131-130">-확인</span><span class="sxs-lookup"><span data-stu-id="e0131-130">-Confirm</span></span>
<span data-ttu-id="e0131-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0131-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0131-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0131-132">-WhatIf</span></span>
<span data-ttu-id="e0131-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e0131-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0131-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e0131-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0131-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0131-135">CommonParameters</span></span>
<span data-ttu-id="e0131-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0131-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0131-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e0131-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0131-138">입력</span><span class="sxs-lookup"><span data-stu-id="e0131-138">INPUTS</span></span>

### <span data-ttu-id="e0131-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e0131-139">System.String</span></span>

### <span data-ttu-id="e0131-140">Microsoft. Azure. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="e0131-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="e0131-141">출력</span><span class="sxs-lookup"><span data-stu-id="e0131-141">OUTPUTS</span></span>

### <span data-ttu-id="e0131-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e0131-142">System.Boolean</span></span>

## <span data-ttu-id="e0131-143">상속자</span><span class="sxs-lookup"><span data-stu-id="e0131-143">NOTES</span></span>

## <span data-ttu-id="e0131-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0131-144">RELATED LINKS</span></span>
