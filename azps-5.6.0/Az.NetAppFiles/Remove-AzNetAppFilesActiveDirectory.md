---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 9ab7607dd358e7c439539e99d44b263136f07cb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968363"
---
# <span data-ttu-id="beaeb-101">Remove-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="beaeb-101">Remove-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="beaeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="beaeb-102">SYNOPSIS</span></span>
<span data-ttu-id="beaeb-103">ANF(Azure NetApp Files) 활성 디렉터리 구성을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="beaeb-103">Deletes an Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="beaeb-104">구문</span><span class="sxs-lookup"><span data-stu-id="beaeb-104">SYNTAX</span></span>

### <span data-ttu-id="beaeb-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="beaeb-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="beaeb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="beaeb-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> -AccountObject <PSNetAppFilesAccount>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="beaeb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="beaeb-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -InputObject <PSNetAppFilesActiveDirectory> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="beaeb-108">설명</span><span class="sxs-lookup"><span data-stu-id="beaeb-108">DESCRIPTION</span></span>
<span data-ttu-id="beaeb-109">**Remove-AzNetAppFilesActiveDirectory** cmdlet은 ANF 활성 디렉터리 구성을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="beaeb-109">The **Remove-AzNetAppFilesActiveDirectory** cmdlet deletes an ANF active directory configuration.</span></span>

## <span data-ttu-id="beaeb-110">예제</span><span class="sxs-lookup"><span data-stu-id="beaeb-110">EXAMPLES</span></span>

### <span data-ttu-id="beaeb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="beaeb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName"
```

<span data-ttu-id="beaeb-112">이 명령은 "MyADName"으로 새 ANF 활성 디렉터리 구성을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="beaeb-112">This command deletes the new ANF active directory configuration with a the name "MyADName".</span></span>

## <span data-ttu-id="beaeb-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="beaeb-113">PARAMETERS</span></span>

### <span data-ttu-id="beaeb-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="beaeb-114">-AccountName</span></span>
<span data-ttu-id="beaeb-115">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="beaeb-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="beaeb-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="beaeb-116">-AccountObject</span></span>
<span data-ttu-id="beaeb-117">Active Directory 개체에 대한 계정</span><span class="sxs-lookup"><span data-stu-id="beaeb-117">The Account for the Active Directory object</span></span>

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

### <span data-ttu-id="beaeb-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="beaeb-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="beaeb-119">ANF 활성 디렉터리의 ID</span><span class="sxs-lookup"><span data-stu-id="beaeb-119">The ID of the ANF active directory</span></span>

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

### <span data-ttu-id="beaeb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beaeb-120">-DefaultProfile</span></span>
<span data-ttu-id="beaeb-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="beaeb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="beaeb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="beaeb-122">-InputObject</span></span>
<span data-ttu-id="beaeb-123">제거할 활성 디렉터리 개체</span><span class="sxs-lookup"><span data-stu-id="beaeb-123">The active directory object to remove</span></span>

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

### <span data-ttu-id="beaeb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="beaeb-124">-PassThru</span></span>
<span data-ttu-id="beaeb-125">지정된 Active Directory가 성공적으로 제거된지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="beaeb-125">Return whether the specified Active Directory  was successfully removed</span></span>

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

### <span data-ttu-id="beaeb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beaeb-126">-ResourceGroupName</span></span>
<span data-ttu-id="beaeb-127">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="beaeb-127">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="beaeb-128">-확인</span><span class="sxs-lookup"><span data-stu-id="beaeb-128">-Confirm</span></span>
<span data-ttu-id="beaeb-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="beaeb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beaeb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beaeb-130">-WhatIf</span></span>
<span data-ttu-id="beaeb-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="beaeb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beaeb-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="beaeb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beaeb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beaeb-133">CommonParameters</span></span>
<span data-ttu-id="beaeb-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="beaeb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beaeb-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="beaeb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beaeb-136">입력</span><span class="sxs-lookup"><span data-stu-id="beaeb-136">INPUTS</span></span>

### <span data-ttu-id="beaeb-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="beaeb-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="beaeb-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="beaeb-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="beaeb-139">출력</span><span class="sxs-lookup"><span data-stu-id="beaeb-139">OUTPUTS</span></span>

### <span data-ttu-id="beaeb-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="beaeb-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="beaeb-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="beaeb-141">NOTES</span></span>

## <span data-ttu-id="beaeb-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="beaeb-142">RELATED LINKS</span></span>
