---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 525483bdb99867ae9403c95a6bc2dc83a855704a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179969"
---
# <span data-ttu-id="c4910-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c4910-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="c4910-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4910-102">SYNOPSIS</span></span>
<span data-ttu-id="c4910-103">제공된 선택적 수정자에 따라 ANF(Azure NetApp Files) 계정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c4910-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="c4910-104">구문</span><span class="sxs-lookup"><span data-stu-id="c4910-104">SYNTAX</span></span>

### <span data-ttu-id="c4910-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c4910-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4910-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4910-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 -ResourceId <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4910-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4910-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] -InputObject <PSNetAppFilesAccount> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4910-108">설명</span><span class="sxs-lookup"><span data-stu-id="c4910-108">DESCRIPTION</span></span>
<span data-ttu-id="c4910-109">**Update-AzNetAppFilesAccount** cmdlet은 ANF 계정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c4910-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="c4910-110">예제</span><span class="sxs-lookup"><span data-stu-id="c4910-110">EXAMPLES</span></span>

### <span data-ttu-id="c4910-111">예제 1: ANF 계정 업데이트</span><span class="sxs-lookup"><span data-stu-id="c4910-111">Example 1 : Updates an ANF account</span></span>
```
PS C:\>Update-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount" -Tag @{'Tag1' = 'Value1'}

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              : {Tag1}
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories :
ProvisioningState : Succeeded
```

<span data-ttu-id="c4910-112">이 명령은 제공된 계정에 대한 태그를 수정하는 업데이트를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4910-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="c4910-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4910-113">PARAMETERS</span></span>

### <span data-ttu-id="c4910-114">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="c4910-114">-ActiveDirectory</span></span>
<span data-ttu-id="c4910-115">활성 감독을 나타내는 해시테이블 배열</span><span class="sxs-lookup"><span data-stu-id="c4910-115">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4910-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4910-116">-DefaultProfile</span></span>
<span data-ttu-id="c4910-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4910-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4910-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4910-118">-InputObject</span></span>
<span data-ttu-id="c4910-119">업데이트할 계정 개체</span><span class="sxs-lookup"><span data-stu-id="c4910-119">The account object to update</span></span>

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

### <span data-ttu-id="c4910-120">-Location</span><span class="sxs-lookup"><span data-stu-id="c4910-120">-Location</span></span>
<span data-ttu-id="c4910-121">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="c4910-121">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4910-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c4910-122">-Name</span></span>
<span data-ttu-id="c4910-123">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="c4910-123">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4910-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4910-124">-ResourceGroupName</span></span>
<span data-ttu-id="c4910-125">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="c4910-125">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4910-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4910-126">-ResourceId</span></span>
<span data-ttu-id="c4910-127">ANF 계정의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c4910-127">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="c4910-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="c4910-128">-Tag</span></span>
<span data-ttu-id="c4910-129">리소스 태그를 나타내는 해시테이블</span><span class="sxs-lookup"><span data-stu-id="c4910-129">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4910-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4910-130">-Confirm</span></span>
<span data-ttu-id="c4910-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4910-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4910-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4910-132">-WhatIf</span></span>
<span data-ttu-id="c4910-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c4910-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4910-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4910-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4910-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4910-135">CommonParameters</span></span>
<span data-ttu-id="c4910-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c4910-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4910-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c4910-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4910-138">입력</span><span class="sxs-lookup"><span data-stu-id="c4910-138">INPUTS</span></span>

### <span data-ttu-id="c4910-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c4910-139">System.String</span></span>

### <span data-ttu-id="c4910-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c4910-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="c4910-141">출력</span><span class="sxs-lookup"><span data-stu-id="c4910-141">OUTPUTS</span></span>

### <span data-ttu-id="c4910-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c4910-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="c4910-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c4910-143">NOTES</span></span>

## <span data-ttu-id="c4910-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4910-144">RELATED LINKS</span></span>
