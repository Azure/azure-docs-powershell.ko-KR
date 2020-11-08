---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 95ed2dc354f32229727a3d1b13dbfdfb95fe001a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048958"
---
# <span data-ttu-id="cd02c-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="cd02c-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="cd02c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd02c-102">SYNOPSIS</span></span>
<span data-ttu-id="cd02c-103">대상 볼륨의 연결을 다시 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd02c-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="cd02c-104">원본 볼륨에서 작업을 실행 하는 경우 연결을 다시 동기화 하 고 원본에서 대상으로 동기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd02c-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="cd02c-105">구문과</span><span class="sxs-lookup"><span data-stu-id="cd02c-105">SYNTAX</span></span>

### <span data-ttu-id="cd02c-106">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="cd02c-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd02c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd02c-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd02c-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd02c-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd02c-109">설명은</span><span class="sxs-lookup"><span data-stu-id="cd02c-109">DESCRIPTION</span></span>
<span data-ttu-id="cd02c-110">대상 볼륨에 대 한 연결 다시 시작/재 동기화</span><span class="sxs-lookup"><span data-stu-id="cd02c-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="cd02c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="cd02c-111">EXAMPLES</span></span>

### <span data-ttu-id="cd02c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="cd02c-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="cd02c-113">이 명령은 "MyDestinationAnfVolume" 볼륨에서 ANF 복제 연결을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd02c-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="cd02c-114">변수</span><span class="sxs-lookup"><span data-stu-id="cd02c-114">PARAMETERS</span></span>

### <span data-ttu-id="cd02c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cd02c-115">-AccountName</span></span>
<span data-ttu-id="cd02c-116">복제 볼륨의 ANF 계정 이름</span><span class="sxs-lookup"><span data-stu-id="cd02c-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="cd02c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd02c-117">-DefaultProfile</span></span>
<span data-ttu-id="cd02c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd02c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd02c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd02c-119">-InputObject</span></span>
<span data-ttu-id="cd02c-120">다시 동기화 할 ANF 복제 대상 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="cd02c-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="cd02c-121">-이름</span><span class="sxs-lookup"><span data-stu-id="cd02c-121">-Name</span></span>
<span data-ttu-id="cd02c-122">ANF 복제 대상 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd02c-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="cd02c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd02c-123">-PassThru</span></span>
<span data-ttu-id="cd02c-124">지정 된 복제 볼륨의 재 동기화가 수행 되었는지 여부 반환</span><span class="sxs-lookup"><span data-stu-id="cd02c-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="cd02c-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="cd02c-125">-PoolName</span></span>
<span data-ttu-id="cd02c-126">복제 볼륨의 ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd02c-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="cd02c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd02c-127">-ResourceGroupName</span></span>
<span data-ttu-id="cd02c-128">ANF 복제 대상 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="cd02c-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="cd02c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd02c-129">-ResourceId</span></span>
<span data-ttu-id="cd02c-130">ANF 복제 대상 볼륨의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="cd02c-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="cd02c-131">-확인</span><span class="sxs-lookup"><span data-stu-id="cd02c-131">-Confirm</span></span>
<span data-ttu-id="cd02c-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd02c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd02c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd02c-133">-WhatIf</span></span>
<span data-ttu-id="cd02c-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cd02c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd02c-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd02c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd02c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd02c-136">CommonParameters</span></span>
<span data-ttu-id="cd02c-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd02c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd02c-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd02c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd02c-139">입력</span><span class="sxs-lookup"><span data-stu-id="cd02c-139">INPUTS</span></span>

### <span data-ttu-id="cd02c-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cd02c-140">System.String</span></span>

### <span data-ttu-id="cd02c-141">Microsoft. Azure. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="cd02c-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="cd02c-142">출력</span><span class="sxs-lookup"><span data-stu-id="cd02c-142">OUTPUTS</span></span>

### <span data-ttu-id="cd02c-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="cd02c-143">System.Boolean</span></span>

## <span data-ttu-id="cd02c-144">상속자</span><span class="sxs-lookup"><span data-stu-id="cd02c-144">NOTES</span></span>

## <span data-ttu-id="cd02c-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd02c-145">RELATED LINKS</span></span>
