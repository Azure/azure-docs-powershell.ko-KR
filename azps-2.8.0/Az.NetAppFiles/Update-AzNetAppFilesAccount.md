---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 46415c4d1671c874135b8d754e9217212ade3838
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870369"
---
# <span data-ttu-id="83adf-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="83adf-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="83adf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83adf-102">SYNOPSIS</span></span>
<span data-ttu-id="83adf-103">제공 되는 선택적 한정자에 따라 ANF (Azure NetApp Files) 계정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="83adf-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="83adf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="83adf-104">SYNTAX</span></span>

```
Update-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-Location <String>]
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```
### <span data-ttu-id="83adf-105">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83adf-105">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83adf-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="83adf-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83adf-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83adf-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83adf-108">설명은</span><span class="sxs-lookup"><span data-stu-id="83adf-108">DESCRIPTION</span></span>
<span data-ttu-id="83adf-109">**업데이트 AzNetAppFilesAccount** cmdlet은 anf 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83adf-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="83adf-110">예제의</span><span class="sxs-lookup"><span data-stu-id="83adf-110">EXAMPLES</span></span>

### <span data-ttu-id="83adf-111">예제 1: ANF 계정 업데이트</span><span class="sxs-lookup"><span data-stu-id="83adf-111">Example 1 : Updates an ANF account</span></span>
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

<span data-ttu-id="83adf-112">이 명령은 제공 된 태그를 수정 하는 지정 된 계정에 대 한 업데이트를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="83adf-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="83adf-113">변수</span><span class="sxs-lookup"><span data-stu-id="83adf-113">PARAMETERS</span></span>

### <span data-ttu-id="83adf-114">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="83adf-114">-ActiveDirectories</span></span>
<span data-ttu-id="83adf-115">Active directory를 나타내는 hashtable 배열</span><span class="sxs-lookup"><span data-stu-id="83adf-115">A hashtable array which represents the active directories</span></span>

```yaml
Type: PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83adf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83adf-116">-DefaultProfile</span></span>
<span data-ttu-id="83adf-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83adf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83adf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83adf-118">-InputObject</span></span>
<span data-ttu-id="83adf-119">업데이트할 account 개체</span><span class="sxs-lookup"><span data-stu-id="83adf-119">The account object to update</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83adf-120">-위치</span><span class="sxs-lookup"><span data-stu-id="83adf-120">-Location</span></span>
<span data-ttu-id="83adf-121">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="83adf-121">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83adf-122">-이름</span><span class="sxs-lookup"><span data-stu-id="83adf-122">-Name</span></span>
<span data-ttu-id="83adf-123">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="83adf-123">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83adf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83adf-124">-ResourceGroupName</span></span>
<span data-ttu-id="83adf-125">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="83adf-125">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83adf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83adf-126">-ResourceId</span></span>
<span data-ttu-id="83adf-127">ANF 계정의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="83adf-127">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="83adf-128">태그</span><span class="sxs-lookup"><span data-stu-id="83adf-128">-Tag</span></span>
<span data-ttu-id="83adf-129">리소스 태그를 나타내는 hashtable</span><span class="sxs-lookup"><span data-stu-id="83adf-129">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83adf-130">-확인</span><span class="sxs-lookup"><span data-stu-id="83adf-130">-Confirm</span></span>
<span data-ttu-id="83adf-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="83adf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83adf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83adf-132">-WhatIf</span></span>
<span data-ttu-id="83adf-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="83adf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83adf-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83adf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83adf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83adf-135">CommonParameters</span></span>
<span data-ttu-id="83adf-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="83adf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="83adf-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83adf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83adf-138">입력</span><span class="sxs-lookup"><span data-stu-id="83adf-138">INPUTS</span></span>

### <span data-ttu-id="83adf-139">않아야</span><span class="sxs-lookup"><span data-stu-id="83adf-139">None</span></span>

## <span data-ttu-id="83adf-140">출력</span><span class="sxs-lookup"><span data-stu-id="83adf-140">OUTPUTS</span></span>

### <span data-ttu-id="83adf-141">Microsoft. p. p. p. p i p. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="83adf-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="83adf-142">상속자</span><span class="sxs-lookup"><span data-stu-id="83adf-142">NOTES</span></span>

## <span data-ttu-id="83adf-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83adf-143">RELATED LINKS</span></span>
