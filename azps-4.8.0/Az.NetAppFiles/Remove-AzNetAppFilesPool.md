---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: 1ab6d38cc5401b4a7e813dafac933d6601a75acd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056645"
---
# <span data-ttu-id="8dfad-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8dfad-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="8dfad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dfad-102">SYNOPSIS</span></span>
<span data-ttu-id="8dfad-103">ANF (Azure NetApp Files) 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dfad-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="8dfad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8dfad-104">SYNTAX</span></span>

### <span data-ttu-id="8dfad-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8dfad-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dfad-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dfad-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dfad-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dfad-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dfad-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dfad-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dfad-109">설명은</span><span class="sxs-lookup"><span data-stu-id="8dfad-109">DESCRIPTION</span></span>
<span data-ttu-id="8dfad-110">**AzNetAppFilesPool** cmdlet은 anf 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dfad-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="8dfad-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8dfad-111">EXAMPLES</span></span>

### <span data-ttu-id="8dfad-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="8dfad-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="8dfad-113">이 명령은 ANF 풀 "MyAnfPool"을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dfad-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="8dfad-114">변수</span><span class="sxs-lookup"><span data-stu-id="8dfad-114">PARAMETERS</span></span>

### <span data-ttu-id="8dfad-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8dfad-115">-AccountName</span></span>
<span data-ttu-id="8dfad-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="8dfad-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="8dfad-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="8dfad-117">-AccountObject</span></span>
<span data-ttu-id="8dfad-118">제거할 풀을 포함 하는 account 개체</span><span class="sxs-lookup"><span data-stu-id="8dfad-118">The account object containing the pool to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dfad-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dfad-119">-DefaultProfile</span></span>
<span data-ttu-id="8dfad-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8dfad-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dfad-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dfad-121">-InputObject</span></span>
<span data-ttu-id="8dfad-122">제거할 풀 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8dfad-122">The pool object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dfad-123">-이름</span><span class="sxs-lookup"><span data-stu-id="8dfad-123">-Name</span></span>
<span data-ttu-id="8dfad-124">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dfad-124">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dfad-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8dfad-125">-PassThru</span></span>
<span data-ttu-id="8dfad-126">지정 된 풀이 성공적으로 제거 되었는지 여부 반환</span><span class="sxs-lookup"><span data-stu-id="8dfad-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="8dfad-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dfad-127">-ResourceGroupName</span></span>
<span data-ttu-id="8dfad-128">ANF 풀의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="8dfad-128">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="8dfad-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dfad-129">-ResourceId</span></span>
<span data-ttu-id="8dfad-130">ANF 풀의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="8dfad-130">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="8dfad-131">-확인</span><span class="sxs-lookup"><span data-stu-id="8dfad-131">-Confirm</span></span>
<span data-ttu-id="8dfad-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dfad-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dfad-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dfad-133">-WhatIf</span></span>
<span data-ttu-id="8dfad-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8dfad-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dfad-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8dfad-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dfad-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dfad-136">CommonParameters</span></span>
<span data-ttu-id="8dfad-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dfad-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dfad-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8dfad-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dfad-139">입력</span><span class="sxs-lookup"><span data-stu-id="8dfad-139">INPUTS</span></span>

### <span data-ttu-id="8dfad-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8dfad-140">System.String</span></span>

### <span data-ttu-id="8dfad-141">Microsoft. p. p. p. p i p. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8dfad-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="8dfad-142">Microsoft. p. p. p. p i p. p i a p. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8dfad-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="8dfad-143">출력</span><span class="sxs-lookup"><span data-stu-id="8dfad-143">OUTPUTS</span></span>

### <span data-ttu-id="8dfad-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8dfad-144">System.Boolean</span></span>

## <span data-ttu-id="8dfad-145">상속자</span><span class="sxs-lookup"><span data-stu-id="8dfad-145">NOTES</span></span>

## <span data-ttu-id="8dfad-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8dfad-146">RELATED LINKS</span></span>
