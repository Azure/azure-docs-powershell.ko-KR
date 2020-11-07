---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 7faa09d45082e6443ab389ebe3a355c9656bb8e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696814"
---
# <span data-ttu-id="5eef8-101">Remove-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5eef8-101">Remove-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="5eef8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eef8-102">SYNOPSIS</span></span>
<span data-ttu-id="5eef8-103">지정 된 Data Lake Store에서 지정 된 가상 네트워크 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5eef8-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="5eef8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5eef8-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5eef8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5eef8-105">DESCRIPTION</span></span>
<span data-ttu-id="5eef8-106">**AzDataLakeStoreVirtualNetworkRule** cmdlet은 지정 된 Data Lake store에서 지정 된 가상 네트워크 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5eef8-106">The **Remove-AzDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="5eef8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5eef8-107">EXAMPLES</span></span>

### <span data-ttu-id="5eef8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5eef8-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="5eef8-109">가상 네트워크 규칙 "myVNET"에서 계정 "dl"을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5eef8-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="5eef8-110">변수</span><span class="sxs-lookup"><span data-stu-id="5eef8-110">PARAMETERS</span></span>

### <span data-ttu-id="5eef8-111">-계정</span><span class="sxs-lookup"><span data-stu-id="5eef8-111">-Account</span></span>
<span data-ttu-id="5eef8-112">의 가상 네트워크 규칙을 업데이트 하기 위한 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="5eef8-112">The Data Lake Store account to update the virtual network rule in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eef8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eef8-113">-DefaultProfile</span></span>
<span data-ttu-id="5eef8-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5eef8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eef8-115">-이름</span><span class="sxs-lookup"><span data-stu-id="5eef8-115">-Name</span></span>
<span data-ttu-id="5eef8-116">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5eef8-116">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eef8-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5eef8-117">-PassThru</span></span>
<span data-ttu-id="5eef8-118">삭제 작업의 결과를 표시 하는 부울 응답을 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5eef8-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="5eef8-119">-확인</span><span class="sxs-lookup"><span data-stu-id="5eef8-119">-Confirm</span></span>
<span data-ttu-id="5eef8-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5eef8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5eef8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eef8-121">-WhatIf</span></span>
<span data-ttu-id="5eef8-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5eef8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5eef8-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5eef8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5eef8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eef8-124">CommonParameters</span></span>
<span data-ttu-id="5eef8-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5eef8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eef8-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eef8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eef8-127">입력</span><span class="sxs-lookup"><span data-stu-id="5eef8-127">INPUTS</span></span>

### <span data-ttu-id="5eef8-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5eef8-128">System.String</span></span>

## <span data-ttu-id="5eef8-129">출력</span><span class="sxs-lookup"><span data-stu-id="5eef8-129">OUTPUTS</span></span>

### <span data-ttu-id="5eef8-130">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="5eef8-130">System.Boolean</span></span>

## <span data-ttu-id="5eef8-131">상속자</span><span class="sxs-lookup"><span data-stu-id="5eef8-131">NOTES</span></span>

## <span data-ttu-id="5eef8-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5eef8-132">RELATED LINKS</span></span>
