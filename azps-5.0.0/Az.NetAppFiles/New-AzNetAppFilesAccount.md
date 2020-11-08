---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 3d23186ce78b2fc97916e029fae8d9db3df1092c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217597"
---
# <span data-ttu-id="7286d-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="7286d-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="7286d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7286d-102">SYNOPSIS</span></span>
<span data-ttu-id="7286d-103">새 Azure NetApp Files (ANF) 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7286d-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="7286d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7286d-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7286d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7286d-105">DESCRIPTION</span></span>
<span data-ttu-id="7286d-106">**새 AzNetAppFilesAccount** cmdlet은 anf 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7286d-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="7286d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7286d-107">EXAMPLES</span></span>

### <span data-ttu-id="7286d-108">예제 1: ANF 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="7286d-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="7286d-109">이 명령은 새 ANF 계정 "MyAnfAccount"을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7286d-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="7286d-110">변수</span><span class="sxs-lookup"><span data-stu-id="7286d-110">PARAMETERS</span></span>

### <span data-ttu-id="7286d-111">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="7286d-111">-ActiveDirectory</span></span>
<span data-ttu-id="7286d-112">Active directory를 나타내는 hashtable 배열</span><span class="sxs-lookup"><span data-stu-id="7286d-112">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="7286d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7286d-113">-DefaultProfile</span></span>
<span data-ttu-id="7286d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7286d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7286d-115">-위치</span><span class="sxs-lookup"><span data-stu-id="7286d-115">-Location</span></span>
<span data-ttu-id="7286d-116">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="7286d-116">The location of the resource</span></span>

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

### <span data-ttu-id="7286d-117">-이름</span><span class="sxs-lookup"><span data-stu-id="7286d-117">-Name</span></span>
<span data-ttu-id="7286d-118">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="7286d-118">The name of the ANF account</span></span>

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

### <span data-ttu-id="7286d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7286d-119">-ResourceGroupName</span></span>
<span data-ttu-id="7286d-120">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="7286d-120">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="7286d-121">태그</span><span class="sxs-lookup"><span data-stu-id="7286d-121">-Tag</span></span>
<span data-ttu-id="7286d-122">리소스 태그를 나타내는 hashtable</span><span class="sxs-lookup"><span data-stu-id="7286d-122">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="7286d-123">-확인</span><span class="sxs-lookup"><span data-stu-id="7286d-123">-Confirm</span></span>
<span data-ttu-id="7286d-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7286d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7286d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7286d-125">-WhatIf</span></span>
<span data-ttu-id="7286d-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7286d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7286d-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7286d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7286d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7286d-128">CommonParameters</span></span>
<span data-ttu-id="7286d-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7286d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7286d-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7286d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7286d-131">입력</span><span class="sxs-lookup"><span data-stu-id="7286d-131">INPUTS</span></span>

### <span data-ttu-id="7286d-132">않아야</span><span class="sxs-lookup"><span data-stu-id="7286d-132">None</span></span>

## <span data-ttu-id="7286d-133">출력</span><span class="sxs-lookup"><span data-stu-id="7286d-133">OUTPUTS</span></span>

### <span data-ttu-id="7286d-134">Microsoft. p. p. p. p i p. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="7286d-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="7286d-135">상속자</span><span class="sxs-lookup"><span data-stu-id="7286d-135">NOTES</span></span>

## <span data-ttu-id="7286d-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7286d-136">RELATED LINKS</span></span>
