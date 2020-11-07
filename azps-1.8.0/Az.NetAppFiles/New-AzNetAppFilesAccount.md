---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 87febe648a845d595f35c1a14b024fbd97824be1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700776"
---
# <span data-ttu-id="40f09-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="40f09-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="40f09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40f09-102">SYNOPSIS</span></span>
<span data-ttu-id="40f09-103">새 Azure NetApp Files (ANF) 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="40f09-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="40f09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="40f09-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40f09-105">설명은</span><span class="sxs-lookup"><span data-stu-id="40f09-105">DESCRIPTION</span></span>
<span data-ttu-id="40f09-106">**새 AzNetAppFilesAccount** cmdlet은 anf 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="40f09-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="40f09-107">예제의</span><span class="sxs-lookup"><span data-stu-id="40f09-107">EXAMPLES</span></span>

### <span data-ttu-id="40f09-108">예제 1: ANF 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="40f09-108">Example 1: Create an ANF account</span></span>
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

<span data-ttu-id="40f09-109">이 명령은 새 ANF 계정 "MyAnfAccount"을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="40f09-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="40f09-110">변수</span><span class="sxs-lookup"><span data-stu-id="40f09-110">PARAMETERS</span></span>

### <span data-ttu-id="40f09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40f09-111">-DefaultProfile</span></span>
<span data-ttu-id="40f09-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40f09-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40f09-113">-위치</span><span class="sxs-lookup"><span data-stu-id="40f09-113">-Location</span></span>
<span data-ttu-id="40f09-114">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="40f09-114">The location of the resource</span></span>

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

### <span data-ttu-id="40f09-115">-이름</span><span class="sxs-lookup"><span data-stu-id="40f09-115">-Name</span></span>
<span data-ttu-id="40f09-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="40f09-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="40f09-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40f09-117">-ResourceGroupName</span></span>
<span data-ttu-id="40f09-118">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="40f09-118">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="40f09-119">태그</span><span class="sxs-lookup"><span data-stu-id="40f09-119">-Tag</span></span>
<span data-ttu-id="40f09-120">리소스 태그를 나타내는 hashtable</span><span class="sxs-lookup"><span data-stu-id="40f09-120">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="40f09-121">-확인</span><span class="sxs-lookup"><span data-stu-id="40f09-121">-Confirm</span></span>
<span data-ttu-id="40f09-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f09-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40f09-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40f09-123">-WhatIf</span></span>
<span data-ttu-id="40f09-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="40f09-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40f09-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40f09-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40f09-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40f09-126">CommonParameters</span></span>
<span data-ttu-id="40f09-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f09-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="40f09-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40f09-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40f09-129">입력</span><span class="sxs-lookup"><span data-stu-id="40f09-129">INPUTS</span></span>

### <span data-ttu-id="40f09-130">않아야</span><span class="sxs-lookup"><span data-stu-id="40f09-130">None</span></span>

## <span data-ttu-id="40f09-131">출력</span><span class="sxs-lookup"><span data-stu-id="40f09-131">OUTPUTS</span></span>

### <span data-ttu-id="40f09-132">Microsoft. p. p. p. p i p. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="40f09-132">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="40f09-133">상속자</span><span class="sxs-lookup"><span data-stu-id="40f09-133">NOTES</span></span>

## <span data-ttu-id="40f09-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40f09-134">RELATED LINKS</span></span>
