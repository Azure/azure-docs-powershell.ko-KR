---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: ecbf6a847ad208b49e11ab0089f9cf486763ddf3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364883"
---
# <span data-ttu-id="a34d9-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a34d9-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="a34d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a34d9-102">SYNOPSIS</span></span>
<span data-ttu-id="a34d9-103">새 데이터 집합으로 ANF(Azure NetApp Files) 계정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a34d9-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="a34d9-104">연결된 활성 디렉터를 지우는 데 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="a34d9-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="a34d9-105">구문</span><span class="sxs-lookup"><span data-stu-id="a34d9-105">SYNTAX</span></span>

### <span data-ttu-id="a34d9-106">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a34d9-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a34d9-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="a34d9-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a34d9-108">설명</span><span class="sxs-lookup"><span data-stu-id="a34d9-108">DESCRIPTION</span></span>
<span data-ttu-id="a34d9-109">**Set-AzNetAppFilesAccount** cmdlet은 ANF 계정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="a34d9-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="a34d9-110">예제</span><span class="sxs-lookup"><span data-stu-id="a34d9-110">EXAMPLES</span></span>

### <span data-ttu-id="a34d9-111">예제 1: ANF 계정 수정</span><span class="sxs-lookup"><span data-stu-id="a34d9-111">Example 1 : Modify an ANF account</span></span>
```
PS C:\>Set-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="a34d9-112">이 명령은 주어진 계정에서 업데이트를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34d9-112">This command performs an update on the given account.</span></span> <span data-ttu-id="a34d9-113">Active Directory가 없는 경우 계정에서 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="a34d9-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="a34d9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a34d9-114">PARAMETERS</span></span>

### <span data-ttu-id="a34d9-115">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="a34d9-115">-ActiveDirectory</span></span>
<span data-ttu-id="a34d9-116">활성 감독을 나타내는 해시테이블 배열</span><span class="sxs-lookup"><span data-stu-id="a34d9-116">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: SetByResourceActiveDirectory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a34d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a34d9-117">-DefaultProfile</span></span>
<span data-ttu-id="a34d9-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a34d9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a34d9-119">-Location</span><span class="sxs-lookup"><span data-stu-id="a34d9-119">-Location</span></span>
<span data-ttu-id="a34d9-120">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="a34d9-120">The location of the resource</span></span>

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

### <span data-ttu-id="a34d9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a34d9-121">-Name</span></span>
<span data-ttu-id="a34d9-122">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="a34d9-122">The name of the ANF account</span></span>

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

### <span data-ttu-id="a34d9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a34d9-123">-ResourceGroupName</span></span>
<span data-ttu-id="a34d9-124">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="a34d9-124">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a34d9-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="a34d9-125">-Tag</span></span>
<span data-ttu-id="a34d9-126">리소스 태그를 나타내는 해시테이블</span><span class="sxs-lookup"><span data-stu-id="a34d9-126">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="a34d9-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a34d9-127">-Confirm</span></span>
<span data-ttu-id="a34d9-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a34d9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a34d9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a34d9-129">-WhatIf</span></span>
<span data-ttu-id="a34d9-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a34d9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a34d9-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a34d9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a34d9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a34d9-132">CommonParameters</span></span>
<span data-ttu-id="a34d9-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a34d9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a34d9-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a34d9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a34d9-135">입력</span><span class="sxs-lookup"><span data-stu-id="a34d9-135">INPUTS</span></span>

### <span data-ttu-id="a34d9-136">없음</span><span class="sxs-lookup"><span data-stu-id="a34d9-136">None</span></span>

## <span data-ttu-id="a34d9-137">출력</span><span class="sxs-lookup"><span data-stu-id="a34d9-137">OUTPUTS</span></span>

### <span data-ttu-id="a34d9-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a34d9-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="a34d9-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a34d9-139">NOTES</span></span>

## <span data-ttu-id="a34d9-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a34d9-140">RELATED LINKS</span></span>
