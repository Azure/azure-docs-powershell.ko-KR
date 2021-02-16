---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 5f6e2421a20cb7aaf044d3abfbbddf7f5c72b37e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180009"
---
# <span data-ttu-id="507f8-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="507f8-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="507f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="507f8-102">SYNOPSIS</span></span>
<span data-ttu-id="507f8-103">ANF(Azure NetApp Files) 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="507f8-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="507f8-104">구문</span><span class="sxs-lookup"><span data-stu-id="507f8-104">SYNTAX</span></span>

### <span data-ttu-id="507f8-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="507f8-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="507f8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="507f8-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="507f8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="507f8-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="507f8-108">설명</span><span class="sxs-lookup"><span data-stu-id="507f8-108">DESCRIPTION</span></span>
<span data-ttu-id="507f8-109">**Remove-AzNetAppFilesAccount** cmdlet은 ANF 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="507f8-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="507f8-110">예제</span><span class="sxs-lookup"><span data-stu-id="507f8-110">EXAMPLES</span></span>

### <span data-ttu-id="507f8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="507f8-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="507f8-112">이 명령은 ANF 계정 "MyAnfAccount"를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="507f8-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="507f8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="507f8-113">PARAMETERS</span></span>

### <span data-ttu-id="507f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="507f8-114">-DefaultProfile</span></span>
<span data-ttu-id="507f8-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="507f8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="507f8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="507f8-116">-InputObject</span></span>
<span data-ttu-id="507f8-117">제거할 계정 개체</span><span class="sxs-lookup"><span data-stu-id="507f8-117">The account object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="507f8-118">-Name</span><span class="sxs-lookup"><span data-stu-id="507f8-118">-Name</span></span>
<span data-ttu-id="507f8-119">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="507f8-119">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507f8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="507f8-120">-PassThru</span></span>
<span data-ttu-id="507f8-121">지정된 계정이 성공적으로 제거됐는지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="507f8-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="507f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="507f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="507f8-123">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="507f8-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="507f8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="507f8-124">-ResourceId</span></span>
<span data-ttu-id="507f8-125">ANF 계정의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="507f8-125">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="507f8-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="507f8-126">-Confirm</span></span>
<span data-ttu-id="507f8-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="507f8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="507f8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="507f8-128">-WhatIf</span></span>
<span data-ttu-id="507f8-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="507f8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="507f8-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="507f8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="507f8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="507f8-131">CommonParameters</span></span>
<span data-ttu-id="507f8-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="507f8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="507f8-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="507f8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="507f8-134">입력</span><span class="sxs-lookup"><span data-stu-id="507f8-134">INPUTS</span></span>

### <span data-ttu-id="507f8-135">System.String</span><span class="sxs-lookup"><span data-stu-id="507f8-135">System.String</span></span>

### <span data-ttu-id="507f8-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="507f8-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="507f8-137">출력</span><span class="sxs-lookup"><span data-stu-id="507f8-137">OUTPUTS</span></span>

### <span data-ttu-id="507f8-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="507f8-138">System.Boolean</span></span>

## <span data-ttu-id="507f8-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="507f8-139">NOTES</span></span>

## <span data-ttu-id="507f8-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="507f8-140">RELATED LINKS</span></span>
