---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: 9400efa61a98b6eb80b975d4999e03eb872e3b28
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218386"
---
# <span data-ttu-id="8ecb4-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8ecb4-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="8ecb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ecb4-102">SYNOPSIS</span></span>
<span data-ttu-id="8ecb4-103">ANF (Azure NetApp Files) 볼륨을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecb4-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="8ecb4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ecb4-104">SYNTAX</span></span>

### <span data-ttu-id="8ecb4-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8ecb4-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ecb4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ecb4-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ecb4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ecb4-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ecb4-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ecb4-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ecb4-109">설명은</span><span class="sxs-lookup"><span data-stu-id="8ecb4-109">DESCRIPTION</span></span>
<span data-ttu-id="8ecb4-110">**AzNetAppFilesVolume** cmdlet은 anf 볼륨을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecb4-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="8ecb4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8ecb4-111">EXAMPLES</span></span>

### <span data-ttu-id="8ecb4-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="8ecb4-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="8ecb4-113">이 명령은 ANF 볼륨 "MyAnfVolume"을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecb4-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="8ecb4-114">변수</span><span class="sxs-lookup"><span data-stu-id="8ecb4-114">PARAMETERS</span></span>

### <span data-ttu-id="8ecb4-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8ecb4-115">-AccountName</span></span>
<span data-ttu-id="8ecb4-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="8ecb4-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="8ecb4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ecb4-117">-DefaultProfile</span></span>
<span data-ttu-id="8ecb4-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ecb4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ecb4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ecb4-119">-InputObject</span></span>
<span data-ttu-id="8ecb4-120">제거할 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="8ecb4-120">The volume object to remove</span></span>

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

### <span data-ttu-id="8ecb4-121">-이름</span><span class="sxs-lookup"><span data-stu-id="8ecb4-121">-Name</span></span>
<span data-ttu-id="8ecb4-122">ANF 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ecb4-122">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecb4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ecb4-123">-PassThru</span></span>
<span data-ttu-id="8ecb4-124">지정 된 볼륨이 성공적으로 제거 되었는지 여부 반환</span><span class="sxs-lookup"><span data-stu-id="8ecb4-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="8ecb4-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="8ecb4-125">-PoolName</span></span>
<span data-ttu-id="8ecb4-126">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ecb4-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="8ecb4-127">-Poo</span><span class="sxs-lookup"><span data-stu-id="8ecb4-127">-PoolObject</span></span>
<span data-ttu-id="8ecb4-128">제거할 볼륨을 포함 하는 pool 개체</span><span class="sxs-lookup"><span data-stu-id="8ecb4-128">The pool object containing the volume to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ecb4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ecb4-129">-ResourceGroupName</span></span>
<span data-ttu-id="8ecb4-130">ANF 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="8ecb4-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="8ecb4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ecb4-131">-ResourceId</span></span>
<span data-ttu-id="8ecb4-132">ANF 볼륨의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="8ecb4-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="8ecb4-133">-확인</span><span class="sxs-lookup"><span data-stu-id="8ecb4-133">-Confirm</span></span>
<span data-ttu-id="8ecb4-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecb4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ecb4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ecb4-135">-WhatIf</span></span>
<span data-ttu-id="8ecb4-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8ecb4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ecb4-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ecb4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ecb4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ecb4-138">CommonParameters</span></span>
<span data-ttu-id="8ecb4-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ecb4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ecb4-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8ecb4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ecb4-141">입력</span><span class="sxs-lookup"><span data-stu-id="8ecb4-141">INPUTS</span></span>

### <span data-ttu-id="8ecb4-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8ecb4-142">System.String</span></span>

### <span data-ttu-id="8ecb4-143">Microsoft. p. p. p. p i p. p i a p. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8ecb4-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="8ecb4-144">Microsoft. Azure. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8ecb4-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="8ecb4-145">출력</span><span class="sxs-lookup"><span data-stu-id="8ecb4-145">OUTPUTS</span></span>

### <span data-ttu-id="8ecb4-146">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8ecb4-146">System.Boolean</span></span>

## <span data-ttu-id="8ecb4-147">상속자</span><span class="sxs-lookup"><span data-stu-id="8ecb4-147">NOTES</span></span>

## <span data-ttu-id="8ecb4-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ecb4-148">RELATED LINKS</span></span>
