---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 5c807c3d134768c7682b2216178eabd5a0771701
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047841"
---
# <span data-ttu-id="a7d20-101">Set-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a7d20-101">Set-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="a7d20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7d20-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d20-103">지정 된 Data Lake Store에서 지정 된 방화벽 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d20-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="a7d20-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7d20-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7d20-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a7d20-105">DESCRIPTION</span></span>
<span data-ttu-id="a7d20-106">**AzDataLakeStoreFirewallRule** cmdlet은 지정 된 Data Lake store에서 지정 된 방화벽 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d20-106">The **Set-AzDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="a7d20-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a7d20-107">EXAMPLES</span></span>

### <span data-ttu-id="a7d20-108">예제 1: 방화벽 규칙의 시작 및 종료 IP 범위 업데이트</span><span class="sxs-lookup"><span data-stu-id="a7d20-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="a7d20-109">"ContosoADL" 계정의 방화벽 규칙 "MyFirewallRule"에서 127.0.0.1-127.0.0.2의 범위를 포함 하도록 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d20-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="a7d20-110">변수</span><span class="sxs-lookup"><span data-stu-id="a7d20-110">PARAMETERS</span></span>

### <span data-ttu-id="a7d20-111">-계정</span><span class="sxs-lookup"><span data-stu-id="a7d20-111">-Account</span></span>
<span data-ttu-id="a7d20-112">방화벽 규칙을 업데이트 하기 위한 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="a7d20-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="a7d20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d20-113">-DefaultProfile</span></span>
<span data-ttu-id="a7d20-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a7d20-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7d20-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="a7d20-115">-EndIpAddress</span></span>
<span data-ttu-id="a7d20-116">방화벽 규칙에 대 한 유효한 ip 범위의 끝</span><span class="sxs-lookup"><span data-stu-id="a7d20-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7d20-117">-이름</span><span class="sxs-lookup"><span data-stu-id="a7d20-117">-Name</span></span>
<span data-ttu-id="a7d20-118">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d20-118">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7d20-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7d20-119">-ResourceGroupName</span></span>
<span data-ttu-id="a7d20-120">방화벽 규칙을 업데이트할 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d20-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7d20-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="a7d20-121">-StartIpAddress</span></span>
<span data-ttu-id="a7d20-122">방화벽 규칙에 대 한 유효한 ip 범위의 시작</span><span class="sxs-lookup"><span data-stu-id="a7d20-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7d20-123">-확인</span><span class="sxs-lookup"><span data-stu-id="a7d20-123">-Confirm</span></span>
<span data-ttu-id="a7d20-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d20-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7d20-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7d20-125">-WhatIf</span></span>
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

### <span data-ttu-id="a7d20-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d20-126">CommonParameters</span></span>
<span data-ttu-id="a7d20-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d20-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d20-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7d20-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d20-129">입력</span><span class="sxs-lookup"><span data-stu-id="a7d20-129">INPUTS</span></span>

### <span data-ttu-id="a7d20-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a7d20-130">System.String</span></span>

## <span data-ttu-id="a7d20-131">출력</span><span class="sxs-lookup"><span data-stu-id="a7d20-131">OUTPUTS</span></span>

### <span data-ttu-id="a7d20-132">DataLakeStore. DataLakeStoreFirewallRule/.</span><span class="sxs-lookup"><span data-stu-id="a7d20-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="a7d20-133">상속자</span><span class="sxs-lookup"><span data-stu-id="a7d20-133">NOTES</span></span>

## <span data-ttu-id="a7d20-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7d20-134">RELATED LINKS</span></span>
