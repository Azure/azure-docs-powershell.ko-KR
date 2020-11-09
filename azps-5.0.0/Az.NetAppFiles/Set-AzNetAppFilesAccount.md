---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: ecbf6a847ad208b49e11ab0089f9cf486763ddf3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309266"
---
# <span data-ttu-id="d13f5-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d13f5-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="d13f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d13f5-102">SYNOPSIS</span></span>
<span data-ttu-id="d13f5-103">새 데이터 집합을 사용 하 여 Azure NetApp Files (ANF) 계정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d13f5-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="d13f5-104">관련 된 active directory를 삭제 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d13f5-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="d13f5-105">구문과</span><span class="sxs-lookup"><span data-stu-id="d13f5-105">SYNTAX</span></span>

### <span data-ttu-id="d13f5-106">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d13f5-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d13f5-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="d13f5-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d13f5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d13f5-108">DESCRIPTION</span></span>
<span data-ttu-id="d13f5-109">**Set-AzNetAppFilesAccount** cmdlet은 anf 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d13f5-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="d13f5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d13f5-110">EXAMPLES</span></span>

### <span data-ttu-id="d13f5-111">예제 1: ANF 계정 수정</span><span class="sxs-lookup"><span data-stu-id="d13f5-111">Example 1 : Modify an ANF account</span></span>
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

<span data-ttu-id="d13f5-112">이 명령은 지정 된 계정에 대 한 업데이트를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d13f5-112">This command performs an update on the given account.</span></span> <span data-ttu-id="d13f5-113">Active directory가 없으면 계정에서 제거 됨을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="d13f5-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="d13f5-114">변수</span><span class="sxs-lookup"><span data-stu-id="d13f5-114">PARAMETERS</span></span>

### <span data-ttu-id="d13f5-115">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="d13f5-115">-ActiveDirectory</span></span>
<span data-ttu-id="d13f5-116">Active directory를 나타내는 hashtable 배열</span><span class="sxs-lookup"><span data-stu-id="d13f5-116">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="d13f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d13f5-117">-DefaultProfile</span></span>
<span data-ttu-id="d13f5-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d13f5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d13f5-119">-위치</span><span class="sxs-lookup"><span data-stu-id="d13f5-119">-Location</span></span>
<span data-ttu-id="d13f5-120">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="d13f5-120">The location of the resource</span></span>

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

### <span data-ttu-id="d13f5-121">-이름</span><span class="sxs-lookup"><span data-stu-id="d13f5-121">-Name</span></span>
<span data-ttu-id="d13f5-122">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="d13f5-122">The name of the ANF account</span></span>

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

### <span data-ttu-id="d13f5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d13f5-123">-ResourceGroupName</span></span>
<span data-ttu-id="d13f5-124">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="d13f5-124">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d13f5-125">태그</span><span class="sxs-lookup"><span data-stu-id="d13f5-125">-Tag</span></span>
<span data-ttu-id="d13f5-126">리소스 태그를 나타내는 hashtable</span><span class="sxs-lookup"><span data-stu-id="d13f5-126">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="d13f5-127">-확인</span><span class="sxs-lookup"><span data-stu-id="d13f5-127">-Confirm</span></span>
<span data-ttu-id="d13f5-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d13f5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d13f5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d13f5-129">-WhatIf</span></span>
<span data-ttu-id="d13f5-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d13f5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d13f5-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d13f5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d13f5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d13f5-132">CommonParameters</span></span>
<span data-ttu-id="d13f5-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d13f5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d13f5-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d13f5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d13f5-135">입력</span><span class="sxs-lookup"><span data-stu-id="d13f5-135">INPUTS</span></span>

### <span data-ttu-id="d13f5-136">않아야</span><span class="sxs-lookup"><span data-stu-id="d13f5-136">None</span></span>

## <span data-ttu-id="d13f5-137">출력</span><span class="sxs-lookup"><span data-stu-id="d13f5-137">OUTPUTS</span></span>

### <span data-ttu-id="d13f5-138">Microsoft. p. p. p. p i p. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d13f5-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="d13f5-139">상속자</span><span class="sxs-lookup"><span data-stu-id="d13f5-139">NOTES</span></span>

## <span data-ttu-id="d13f5-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d13f5-140">RELATED LINKS</span></span>
