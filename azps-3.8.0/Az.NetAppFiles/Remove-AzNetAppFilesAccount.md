---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: de0f71a91ec4445ae4be58e904e58eb3a97cb9a0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877281"
---
# <span data-ttu-id="aefcd-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="aefcd-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="aefcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aefcd-102">SYNOPSIS</span></span>
<span data-ttu-id="aefcd-103">ANF (Azure NetApp Files) 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aefcd-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="aefcd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aefcd-104">SYNTAX</span></span>

### <span data-ttu-id="aefcd-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="aefcd-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aefcd-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aefcd-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aefcd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aefcd-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aefcd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="aefcd-108">DESCRIPTION</span></span>
<span data-ttu-id="aefcd-109">**AzNetAppFilesAccount** cmdlet은 anf 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aefcd-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="aefcd-110">예제의</span><span class="sxs-lookup"><span data-stu-id="aefcd-110">EXAMPLES</span></span>

### <span data-ttu-id="aefcd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="aefcd-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="aefcd-112">이 명령은 ANF 계정 "MyAnfAccount"을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aefcd-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="aefcd-113">변수</span><span class="sxs-lookup"><span data-stu-id="aefcd-113">PARAMETERS</span></span>

### <span data-ttu-id="aefcd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aefcd-114">-DefaultProfile</span></span>
<span data-ttu-id="aefcd-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aefcd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aefcd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aefcd-116">-InputObject</span></span>
<span data-ttu-id="aefcd-117">제거할 account 개체</span><span class="sxs-lookup"><span data-stu-id="aefcd-117">The account object to remove</span></span>

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

### <span data-ttu-id="aefcd-118">-이름</span><span class="sxs-lookup"><span data-stu-id="aefcd-118">-Name</span></span>
<span data-ttu-id="aefcd-119">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="aefcd-119">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefcd-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aefcd-120">-PassThru</span></span>
<span data-ttu-id="aefcd-121">지정 된 계정이 성공적으로 제거 되었는지 여부 반환</span><span class="sxs-lookup"><span data-stu-id="aefcd-121">Return whether the specified account was successfully removed</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefcd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aefcd-122">-ResourceGroupName</span></span>
<span data-ttu-id="aefcd-123">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="aefcd-123">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefcd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aefcd-124">-ResourceId</span></span>
<span data-ttu-id="aefcd-125">ANF 계정의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="aefcd-125">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="aefcd-126">-확인</span><span class="sxs-lookup"><span data-stu-id="aefcd-126">-Confirm</span></span>
<span data-ttu-id="aefcd-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aefcd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aefcd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aefcd-128">-WhatIf</span></span>
<span data-ttu-id="aefcd-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aefcd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aefcd-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aefcd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aefcd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aefcd-131">CommonParameters</span></span>
<span data-ttu-id="aefcd-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aefcd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="aefcd-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aefcd-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aefcd-134">입력</span><span class="sxs-lookup"><span data-stu-id="aefcd-134">INPUTS</span></span>

### <span data-ttu-id="aefcd-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aefcd-135">System.String</span></span>

### <span data-ttu-id="aefcd-136">Microsoft. p. p. p. p i p. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="aefcd-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="aefcd-137">출력</span><span class="sxs-lookup"><span data-stu-id="aefcd-137">OUTPUTS</span></span>

### <span data-ttu-id="aefcd-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="aefcd-138">System.Boolean</span></span>

## <span data-ttu-id="aefcd-139">상속자</span><span class="sxs-lookup"><span data-stu-id="aefcd-139">NOTES</span></span>

## <span data-ttu-id="aefcd-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aefcd-140">RELATED LINKS</span></span>
