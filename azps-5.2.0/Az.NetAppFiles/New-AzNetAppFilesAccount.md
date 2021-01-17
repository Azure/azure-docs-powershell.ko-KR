---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 3d23186ce78b2fc97916e029fae8d9db3df1092c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360011"
---
# <span data-ttu-id="9ddc9-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="9ddc9-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="9ddc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ddc9-102">SYNOPSIS</span></span>
<span data-ttu-id="9ddc9-103">새 ANF(Azure NetApp Files) 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ddc9-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="9ddc9-104">구문</span><span class="sxs-lookup"><span data-stu-id="9ddc9-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ddc9-105">설명</span><span class="sxs-lookup"><span data-stu-id="9ddc9-105">DESCRIPTION</span></span>
<span data-ttu-id="9ddc9-106">**New-AzNetAppFilesAccount** cmdlet은 ANF 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ddc9-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="9ddc9-107">예제</span><span class="sxs-lookup"><span data-stu-id="9ddc9-107">EXAMPLES</span></span>

### <span data-ttu-id="9ddc9-108">예제 1: ANF 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="9ddc9-108">Example 1: Create an ANF account</span></span>
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

<span data-ttu-id="9ddc9-109">이 명령은 새 ANF 계정 "MyAnfAccount"를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ddc9-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="9ddc9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ddc9-110">PARAMETERS</span></span>

### <span data-ttu-id="9ddc9-111">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="9ddc9-111">-ActiveDirectory</span></span>
<span data-ttu-id="9ddc9-112">활성 감독을 나타내는 해시테이블 배열</span><span class="sxs-lookup"><span data-stu-id="9ddc9-112">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="9ddc9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ddc9-113">-DefaultProfile</span></span>
<span data-ttu-id="9ddc9-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ddc9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ddc9-115">-Location</span><span class="sxs-lookup"><span data-stu-id="9ddc9-115">-Location</span></span>
<span data-ttu-id="9ddc9-116">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="9ddc9-116">The location of the resource</span></span>

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

### <span data-ttu-id="9ddc9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9ddc9-117">-Name</span></span>
<span data-ttu-id="9ddc9-118">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="9ddc9-118">The name of the ANF account</span></span>

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

### <span data-ttu-id="9ddc9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ddc9-119">-ResourceGroupName</span></span>
<span data-ttu-id="9ddc9-120">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="9ddc9-120">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="9ddc9-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="9ddc9-121">-Tag</span></span>
<span data-ttu-id="9ddc9-122">리소스 태그를 나타내는 해시테이블</span><span class="sxs-lookup"><span data-stu-id="9ddc9-122">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="9ddc9-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ddc9-123">-Confirm</span></span>
<span data-ttu-id="9ddc9-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ddc9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ddc9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ddc9-125">-WhatIf</span></span>
<span data-ttu-id="9ddc9-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9ddc9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ddc9-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ddc9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ddc9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ddc9-128">CommonParameters</span></span>
<span data-ttu-id="9ddc9-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9ddc9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ddc9-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9ddc9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ddc9-131">입력</span><span class="sxs-lookup"><span data-stu-id="9ddc9-131">INPUTS</span></span>

### <span data-ttu-id="9ddc9-132">없음</span><span class="sxs-lookup"><span data-stu-id="9ddc9-132">None</span></span>

## <span data-ttu-id="9ddc9-133">출력</span><span class="sxs-lookup"><span data-stu-id="9ddc9-133">OUTPUTS</span></span>

### <span data-ttu-id="9ddc9-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="9ddc9-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="9ddc9-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9ddc9-135">NOTES</span></span>

## <span data-ttu-id="9ddc9-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ddc9-136">RELATED LINKS</span></span>
