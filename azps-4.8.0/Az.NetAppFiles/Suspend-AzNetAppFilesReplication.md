---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: eb695da1dc1fea238a57ea1c98bec42899e8f28f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211615"
---
# <span data-ttu-id="74520-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="74520-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="74520-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74520-102">SYNOPSIS</span></span>
<span data-ttu-id="74520-103">대상 볼륨에서 복제 연결 일시 중단/중단</span><span class="sxs-lookup"><span data-stu-id="74520-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="74520-104">구문과</span><span class="sxs-lookup"><span data-stu-id="74520-104">SYNTAX</span></span>

### <span data-ttu-id="74520-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="74520-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74520-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74520-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74520-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74520-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74520-108">설명은</span><span class="sxs-lookup"><span data-stu-id="74520-108">DESCRIPTION</span></span>
<span data-ttu-id="74520-109">대상 볼륨에서 복제 연결 일시 중단/중단</span><span class="sxs-lookup"><span data-stu-id="74520-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="74520-110">예제의</span><span class="sxs-lookup"><span data-stu-id="74520-110">EXAMPLES</span></span>

### <span data-ttu-id="74520-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="74520-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="74520-112">이 명령은 "MyDestinationAnfVolume" 볼륨에서 ANF 복제 연결을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="74520-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="74520-113">변수</span><span class="sxs-lookup"><span data-stu-id="74520-113">PARAMETERS</span></span>

### <span data-ttu-id="74520-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="74520-114">-AccountName</span></span>
<span data-ttu-id="74520-115">복제 볼륨의 ANF 계정 이름</span><span class="sxs-lookup"><span data-stu-id="74520-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="74520-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74520-116">-DefaultProfile</span></span>
<span data-ttu-id="74520-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="74520-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74520-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74520-118">-InputObject</span></span>
<span data-ttu-id="74520-119">복제를 중단할 ANF 대상 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="74520-119">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="74520-120">-이름</span><span class="sxs-lookup"><span data-stu-id="74520-120">-Name</span></span>
<span data-ttu-id="74520-121">ANF 복제 대상 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="74520-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="74520-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74520-122">-PassThru</span></span>
<span data-ttu-id="74520-123">지정 된 볼륨 복제 중단이 수행 되었는지 여부 반환</span><span class="sxs-lookup"><span data-stu-id="74520-123">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="74520-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="74520-124">-PoolName</span></span>
<span data-ttu-id="74520-125">복제 볼륨의 ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="74520-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="74520-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74520-126">-ResourceGroupName</span></span>
<span data-ttu-id="74520-127">ANF 복제 대상 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="74520-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="74520-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74520-128">-ResourceId</span></span>
<span data-ttu-id="74520-129">ANF 복제 대상 볼륨의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="74520-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="74520-130">-확인</span><span class="sxs-lookup"><span data-stu-id="74520-130">-Confirm</span></span>
<span data-ttu-id="74520-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="74520-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74520-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74520-132">-WhatIf</span></span>
<span data-ttu-id="74520-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="74520-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74520-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="74520-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74520-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74520-135">CommonParameters</span></span>
<span data-ttu-id="74520-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="74520-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74520-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="74520-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74520-138">입력</span><span class="sxs-lookup"><span data-stu-id="74520-138">INPUTS</span></span>

### <span data-ttu-id="74520-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="74520-139">System.String</span></span>

### <span data-ttu-id="74520-140">Microsoft. Azure. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="74520-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="74520-141">출력</span><span class="sxs-lookup"><span data-stu-id="74520-141">OUTPUTS</span></span>

### <span data-ttu-id="74520-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="74520-142">System.Boolean</span></span>

## <span data-ttu-id="74520-143">상속자</span><span class="sxs-lookup"><span data-stu-id="74520-143">NOTES</span></span>

## <span data-ttu-id="74520-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="74520-144">RELATED LINKS</span></span>
