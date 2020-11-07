---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: 717c1cac6def6fb51f1ab8b598f15a05a7d62db4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877279"
---
# <span data-ttu-id="24e98-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="24e98-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="24e98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24e98-102">SYNOPSIS</span></span>
<span data-ttu-id="24e98-103">ANF (Azure NetApp Files) 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="24e98-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="24e98-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24e98-104">SYNTAX</span></span>

### <span data-ttu-id="24e98-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="24e98-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24e98-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24e98-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24e98-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24e98-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24e98-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24e98-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24e98-109">설명은</span><span class="sxs-lookup"><span data-stu-id="24e98-109">DESCRIPTION</span></span>
<span data-ttu-id="24e98-110">**AzNetAppFilesPool** cmdlet은 anf 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="24e98-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="24e98-111">예제의</span><span class="sxs-lookup"><span data-stu-id="24e98-111">EXAMPLES</span></span>

### <span data-ttu-id="24e98-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="24e98-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="24e98-113">이 명령은 ANF 풀 "MyAnfPool"을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="24e98-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="24e98-114">변수</span><span class="sxs-lookup"><span data-stu-id="24e98-114">PARAMETERS</span></span>

### <span data-ttu-id="24e98-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="24e98-115">-AccountName</span></span>
<span data-ttu-id="24e98-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="24e98-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="24e98-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="24e98-117">-AccountObject</span></span>
<span data-ttu-id="24e98-118">제거할 풀을 포함 하는 account 개체</span><span class="sxs-lookup"><span data-stu-id="24e98-118">The account object containing the pool to remove</span></span>

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

### <span data-ttu-id="24e98-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24e98-119">-DefaultProfile</span></span>
<span data-ttu-id="24e98-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24e98-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24e98-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24e98-121">-InputObject</span></span>
<span data-ttu-id="24e98-122">제거할 풀 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="24e98-122">The pool object to remove</span></span>

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

### <span data-ttu-id="24e98-123">-이름</span><span class="sxs-lookup"><span data-stu-id="24e98-123">-Name</span></span>
<span data-ttu-id="24e98-124">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24e98-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="24e98-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24e98-125">-PassThru</span></span>
<span data-ttu-id="24e98-126">지정 된 풀이 성공적으로 제거 되었는지 여부 반환</span><span class="sxs-lookup"><span data-stu-id="24e98-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="24e98-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24e98-127">-ResourceGroupName</span></span>
<span data-ttu-id="24e98-128">ANF 풀의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="24e98-128">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="24e98-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24e98-129">-ResourceId</span></span>
<span data-ttu-id="24e98-130">ANF 풀의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="24e98-130">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="24e98-131">-확인</span><span class="sxs-lookup"><span data-stu-id="24e98-131">-Confirm</span></span>
<span data-ttu-id="24e98-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24e98-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24e98-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24e98-133">-WhatIf</span></span>
<span data-ttu-id="24e98-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24e98-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24e98-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24e98-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24e98-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e98-136">CommonParameters</span></span>
<span data-ttu-id="24e98-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24e98-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="24e98-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24e98-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e98-139">입력</span><span class="sxs-lookup"><span data-stu-id="24e98-139">INPUTS</span></span>

### <span data-ttu-id="24e98-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24e98-140">System.String</span></span>

### <span data-ttu-id="24e98-141">Microsoft. p. p. p. p i p. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="24e98-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="24e98-142">Microsoft. p. p. p. p i p. p i a p. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="24e98-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="24e98-143">출력</span><span class="sxs-lookup"><span data-stu-id="24e98-143">OUTPUTS</span></span>

### <span data-ttu-id="24e98-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="24e98-144">System.Boolean</span></span>

## <span data-ttu-id="24e98-145">상속자</span><span class="sxs-lookup"><span data-stu-id="24e98-145">NOTES</span></span>

## <span data-ttu-id="24e98-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24e98-146">RELATED LINKS</span></span>
