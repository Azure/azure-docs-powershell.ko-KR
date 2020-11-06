---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
ms.openlocfilehash: 1d4a5365ac2112364a544eb2481a3193f23519c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532823"
---
# <span data-ttu-id="42b69-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="42b69-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="42b69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42b69-102">SYNOPSIS</span></span>
<span data-ttu-id="42b69-103">작업 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b69-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42b69-104">구문과</span><span class="sxs-lookup"><span data-stu-id="42b69-104">SYNTAX</span></span>

### <span data-ttu-id="42b69-105">ByPropertyName (기본값)</span><span class="sxs-lookup"><span data-stu-id="42b69-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42b69-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="42b69-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42b69-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="42b69-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42b69-108">설명은</span><span class="sxs-lookup"><span data-stu-id="42b69-108">DESCRIPTION</span></span>
<span data-ttu-id="42b69-109">**제거-AzureRmActionGroup** cmdlet은 작업 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b69-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="42b69-110">예제의</span><span class="sxs-lookup"><span data-stu-id="42b69-110">EXAMPLES</span></span>

### <span data-ttu-id="42b69-111">예제 1: 작업 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="42b69-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="42b69-112">변수</span><span class="sxs-lookup"><span data-stu-id="42b69-112">PARAMETERS</span></span>

### <span data-ttu-id="42b69-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42b69-113">-DefaultProfile</span></span>
<span data-ttu-id="42b69-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="42b69-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b69-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42b69-115">-InputObject</span></span>
<span data-ttu-id="42b69-116">작업 그룹 resourc</span><span class="sxs-lookup"><span data-stu-id="42b69-116">The action group resourc</span></span>

```yaml
Type: PSActionGroupResource
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42b69-117">-이름</span><span class="sxs-lookup"><span data-stu-id="42b69-117">-Name</span></span>
<span data-ttu-id="42b69-118">작업 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42b69-118">The name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b69-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42b69-119">-ResourceGroupName</span></span>
<span data-ttu-id="42b69-120">자원 그룹 베트남</span><span class="sxs-lookup"><span data-stu-id="42b69-120">The resource group nam</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b69-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42b69-121">-ResourceId</span></span>
<span data-ttu-id="42b69-122">리소스 i</span><span class="sxs-lookup"><span data-stu-id="42b69-122">The resource i</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b69-123">-확인</span><span class="sxs-lookup"><span data-stu-id="42b69-123">-Confirm</span></span>
<span data-ttu-id="42b69-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b69-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42b69-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42b69-125">-WhatIf</span></span>
<span data-ttu-id="42b69-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="42b69-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42b69-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42b69-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42b69-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42b69-128">CommonParameters</span></span>
<span data-ttu-id="42b69-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b69-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42b69-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42b69-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42b69-131">입력</span><span class="sxs-lookup"><span data-stu-id="42b69-131">INPUTS</span></span>

### <span data-ttu-id="42b69-132">않아야</span><span class="sxs-lookup"><span data-stu-id="42b69-132">None</span></span>
<span data-ttu-id="42b69-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42b69-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="42b69-134">출력</span><span class="sxs-lookup"><span data-stu-id="42b69-134">OUTPUTS</span></span>

### <span data-ttu-id="42b69-135">Microsoft Azure AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="42b69-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="42b69-136">상속자</span><span class="sxs-lookup"><span data-stu-id="42b69-136">NOTES</span></span>

## <span data-ttu-id="42b69-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42b69-137">RELATED LINKS</span></span>

<span data-ttu-id="42b69-138">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [새로운 AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="42b69-138">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
