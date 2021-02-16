---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 7fcf1f749816872fb7407fedaea10d06f3385441
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179985"
---
# <span data-ttu-id="43ed2-101">Remove-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="43ed2-101">Remove-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="43ed2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="43ed2-103">ANF(Azure NetApp Files) Active Directory 구성을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="43ed2-103">Deletes an Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="43ed2-104">구문</span><span class="sxs-lookup"><span data-stu-id="43ed2-104">SYNTAX</span></span>

### <span data-ttu-id="43ed2-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="43ed2-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43ed2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43ed2-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> -AccountObject <PSNetAppFilesAccount>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43ed2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43ed2-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -InputObject <PSNetAppFilesActiveDirectory> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43ed2-108">설명</span><span class="sxs-lookup"><span data-stu-id="43ed2-108">DESCRIPTION</span></span>
<span data-ttu-id="43ed2-109">**Remove-AzNetAppFilesActiveDirectory** cmdlet은 ANF Active Directory 구성을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="43ed2-109">The **Remove-AzNetAppFilesActiveDirectory** cmdlet deletes an ANF active directory configuration.</span></span>

## <span data-ttu-id="43ed2-110">예제</span><span class="sxs-lookup"><span data-stu-id="43ed2-110">EXAMPLES</span></span>

### <span data-ttu-id="43ed2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="43ed2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName"
```

<span data-ttu-id="43ed2-112">이 명령은 이름이 "MyADName"인 새 ANF Active Directory 구성을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="43ed2-112">This command deletes the new ANF active directory configuration with a the name "MyADName".</span></span>

## <span data-ttu-id="43ed2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43ed2-113">PARAMETERS</span></span>

### <span data-ttu-id="43ed2-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="43ed2-114">-AccountName</span></span>
<span data-ttu-id="43ed2-115">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="43ed2-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="43ed2-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="43ed2-116">-AccountObject</span></span>
<span data-ttu-id="43ed2-117">Active Directory 개체에 대한 계정</span><span class="sxs-lookup"><span data-stu-id="43ed2-117">The Account for the Active Directory object</span></span>

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

### <span data-ttu-id="43ed2-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="43ed2-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="43ed2-119">ANF Active Directory의 ID</span><span class="sxs-lookup"><span data-stu-id="43ed2-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ed2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43ed2-120">-DefaultProfile</span></span>
<span data-ttu-id="43ed2-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="43ed2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43ed2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43ed2-122">-InputObject</span></span>
<span data-ttu-id="43ed2-123">제거할 Active Directory 개체</span><span class="sxs-lookup"><span data-stu-id="43ed2-123">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43ed2-124">-PassThru</span></span>
<span data-ttu-id="43ed2-125">지정된 Active Directory가 성공적으로 제거됐는지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="43ed2-125">Return whether the specified Active Directory  was successfully removed</span></span>

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

### <span data-ttu-id="43ed2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43ed2-126">-ResourceGroupName</span></span>
<span data-ttu-id="43ed2-127">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="43ed2-127">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="43ed2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43ed2-128">-Confirm</span></span>
<span data-ttu-id="43ed2-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="43ed2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43ed2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43ed2-130">-WhatIf</span></span>
<span data-ttu-id="43ed2-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="43ed2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43ed2-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43ed2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43ed2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ed2-133">CommonParameters</span></span>
<span data-ttu-id="43ed2-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="43ed2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ed2-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="43ed2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ed2-136">입력</span><span class="sxs-lookup"><span data-stu-id="43ed2-136">INPUTS</span></span>

### <span data-ttu-id="43ed2-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="43ed2-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="43ed2-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="43ed2-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="43ed2-139">출력</span><span class="sxs-lookup"><span data-stu-id="43ed2-139">OUTPUTS</span></span>

### <span data-ttu-id="43ed2-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="43ed2-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="43ed2-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="43ed2-141">NOTES</span></span>

## <span data-ttu-id="43ed2-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43ed2-142">RELATED LINKS</span></span>
