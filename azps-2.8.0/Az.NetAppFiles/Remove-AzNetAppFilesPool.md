---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: ef896185b606e107bb62208255a255655814fcbc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870381"
---
# <span data-ttu-id="8ba2f-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8ba2f-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="8ba2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ba2f-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba2f-103">ANF (Azure NetApp Files) 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ba2f-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="8ba2f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ba2f-104">SYNTAX</span></span>

### <span data-ttu-id="8ba2f-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8ba2f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ba2f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ba2f-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ba2f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ba2f-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ba2f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ba2f-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ba2f-109">설명은</span><span class="sxs-lookup"><span data-stu-id="8ba2f-109">DESCRIPTION</span></span>
<span data-ttu-id="8ba2f-110">**AzNetAppFilesPool** cmdlet은 anf 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ba2f-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="8ba2f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8ba2f-111">EXAMPLES</span></span>

### <span data-ttu-id="8ba2f-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="8ba2f-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="8ba2f-113">이 명령은 ANF 풀 "MyAnfPool"을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ba2f-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="8ba2f-114">변수</span><span class="sxs-lookup"><span data-stu-id="8ba2f-114">PARAMETERS</span></span>

### <span data-ttu-id="8ba2f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8ba2f-115">-AccountName</span></span>
<span data-ttu-id="8ba2f-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="8ba2f-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba2f-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="8ba2f-117">-AccountObject</span></span>
<span data-ttu-id="8ba2f-118">제거할 풀을 포함 하는 account 개체</span><span class="sxs-lookup"><span data-stu-id="8ba2f-118">The account object containing the pool to remove</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba2f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba2f-119">-DefaultProfile</span></span>
<span data-ttu-id="8ba2f-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ba2f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba2f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ba2f-121">-InputObject</span></span>
<span data-ttu-id="8ba2f-122">제거할 풀 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8ba2f-122">The pool object to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba2f-123">-이름</span><span class="sxs-lookup"><span data-stu-id="8ba2f-123">-Name</span></span>
<span data-ttu-id="8ba2f-124">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ba2f-124">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba2f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ba2f-125">-PassThru</span></span>
<span data-ttu-id="8ba2f-126">지정 된 풀이 성공적으로 제거 되었는지 여부 반환</span><span class="sxs-lookup"><span data-stu-id="8ba2f-126">Return whether the specified pool was successfully removed</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba2f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ba2f-127">-ResourceGroupName</span></span>
<span data-ttu-id="8ba2f-128">ANF 풀의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="8ba2f-128">The resource group of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba2f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ba2f-129">-ResourceId</span></span>
<span data-ttu-id="8ba2f-130">ANF 풀의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="8ba2f-130">The resource id of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba2f-131">-확인</span><span class="sxs-lookup"><span data-stu-id="8ba2f-131">-Confirm</span></span>
<span data-ttu-id="8ba2f-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ba2f-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba2f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ba2f-133">-WhatIf</span></span>
<span data-ttu-id="8ba2f-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8ba2f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ba2f-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ba2f-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba2f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba2f-136">CommonParameters</span></span>
<span data-ttu-id="8ba2f-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ba2f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8ba2f-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ba2f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba2f-139">입력</span><span class="sxs-lookup"><span data-stu-id="8ba2f-139">INPUTS</span></span>

### <span data-ttu-id="8ba2f-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8ba2f-140">System.String</span></span>

### <span data-ttu-id="8ba2f-141">Microsoft. p. p. p. p i p. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8ba2f-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="8ba2f-142">Microsoft. p. p. p. p i p. p i a p. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8ba2f-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="8ba2f-143">출력</span><span class="sxs-lookup"><span data-stu-id="8ba2f-143">OUTPUTS</span></span>

### <span data-ttu-id="8ba2f-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8ba2f-144">System.Boolean</span></span>

## <span data-ttu-id="8ba2f-145">상속자</span><span class="sxs-lookup"><span data-stu-id="8ba2f-145">NOTES</span></span>

## <span data-ttu-id="8ba2f-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ba2f-146">RELATED LINKS</span></span>
