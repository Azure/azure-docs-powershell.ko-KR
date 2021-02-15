---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 3d23186ce78b2fc97916e029fae8d9db3df1092c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184860"
---
# <span data-ttu-id="28cce-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="28cce-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="28cce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28cce-102">SYNOPSIS</span></span>
<span data-ttu-id="28cce-103">새 ANF(Azure NetApp Files) 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="28cce-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="28cce-104">구문</span><span class="sxs-lookup"><span data-stu-id="28cce-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28cce-105">설명</span><span class="sxs-lookup"><span data-stu-id="28cce-105">DESCRIPTION</span></span>
<span data-ttu-id="28cce-106">**New-AzNetAppFilesAccount** cmdlet은 ANF 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="28cce-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="28cce-107">예제</span><span class="sxs-lookup"><span data-stu-id="28cce-107">EXAMPLES</span></span>

### <span data-ttu-id="28cce-108">예제 1: ANF 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="28cce-108">Example 1: Create an ANF account</span></span>
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

<span data-ttu-id="28cce-109">이 명령은 새 ANF 계정 "MyAnfAccount"를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="28cce-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="28cce-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28cce-110">PARAMETERS</span></span>

### <span data-ttu-id="28cce-111">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="28cce-111">-ActiveDirectory</span></span>
<span data-ttu-id="28cce-112">활성 감독을 나타내는 해시테이블 배열</span><span class="sxs-lookup"><span data-stu-id="28cce-112">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="28cce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28cce-113">-DefaultProfile</span></span>
<span data-ttu-id="28cce-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28cce-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28cce-115">-Location</span><span class="sxs-lookup"><span data-stu-id="28cce-115">-Location</span></span>
<span data-ttu-id="28cce-116">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="28cce-116">The location of the resource</span></span>

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

### <span data-ttu-id="28cce-117">-Name</span><span class="sxs-lookup"><span data-stu-id="28cce-117">-Name</span></span>
<span data-ttu-id="28cce-118">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="28cce-118">The name of the ANF account</span></span>

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

### <span data-ttu-id="28cce-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28cce-119">-ResourceGroupName</span></span>
<span data-ttu-id="28cce-120">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="28cce-120">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="28cce-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="28cce-121">-Tag</span></span>
<span data-ttu-id="28cce-122">리소스 태그를 나타내는 해시테이블</span><span class="sxs-lookup"><span data-stu-id="28cce-122">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="28cce-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28cce-123">-Confirm</span></span>
<span data-ttu-id="28cce-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="28cce-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28cce-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28cce-125">-WhatIf</span></span>
<span data-ttu-id="28cce-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="28cce-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28cce-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28cce-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28cce-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28cce-128">CommonParameters</span></span>
<span data-ttu-id="28cce-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="28cce-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28cce-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="28cce-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28cce-131">입력</span><span class="sxs-lookup"><span data-stu-id="28cce-131">INPUTS</span></span>

### <span data-ttu-id="28cce-132">없음</span><span class="sxs-lookup"><span data-stu-id="28cce-132">None</span></span>

## <span data-ttu-id="28cce-133">출력</span><span class="sxs-lookup"><span data-stu-id="28cce-133">OUTPUTS</span></span>

### <span data-ttu-id="28cce-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="28cce-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="28cce-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="28cce-135">NOTES</span></span>

## <span data-ttu-id="28cce-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28cce-136">RELATED LINKS</span></span>
