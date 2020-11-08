---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: a51345653580261178191687f54bf0f2a8cc6f0c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214081"
---
# <span data-ttu-id="06202-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="06202-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="06202-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06202-102">SYNOPSIS</span></span>
<span data-ttu-id="06202-103">Azure SecurityPartnerProvider를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="06202-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="06202-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06202-104">SYNTAX</span></span>

### <span data-ttu-id="06202-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="06202-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06202-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06202-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06202-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="06202-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06202-108">설명은</span><span class="sxs-lookup"><span data-stu-id="06202-108">DESCRIPTION</span></span>
<span data-ttu-id="06202-109">**AzSecurityPartnerProvider** Cmdlet은 Azure SecurityPartnerProvider를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="06202-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="06202-110">예제의</span><span class="sxs-lookup"><span data-stu-id="06202-110">EXAMPLES</span></span>

### <span data-ttu-id="06202-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="06202-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="06202-112">변수</span><span class="sxs-lookup"><span data-stu-id="06202-112">PARAMETERS</span></span>

### <span data-ttu-id="06202-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06202-113">-AsJob</span></span>
<span data-ttu-id="06202-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="06202-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06202-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06202-115">-DefaultProfile</span></span>
<span data-ttu-id="06202-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06202-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06202-117">-Force</span><span class="sxs-lookup"><span data-stu-id="06202-117">-Force</span></span>
<span data-ttu-id="06202-118">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06202-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="06202-119">-이름</span><span class="sxs-lookup"><span data-stu-id="06202-119">-Name</span></span>
<span data-ttu-id="06202-120">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06202-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06202-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06202-121">-PassThru</span></span>
<span data-ttu-id="06202-122">이 작업이 수행 되는 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="06202-122">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="06202-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06202-123">-ResourceGroupName</span></span>
<span data-ttu-id="06202-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06202-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06202-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06202-125">-ResourceId</span></span>
<span data-ttu-id="06202-126">SecurityPartnerProvider 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="06202-126">The securityPartnerProvider resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06202-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="06202-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="06202-128">SecurityPartnerProvider input 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="06202-128">The securityPartnerProvider input object.</span></span>

```yaml
Type: PSSecurityPartnerProvider
Parameter Sets: SecurityPartnerProviderInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06202-129">-확인</span><span class="sxs-lookup"><span data-stu-id="06202-129">-Confirm</span></span>
<span data-ttu-id="06202-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="06202-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06202-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06202-131">-WhatIf</span></span>
<span data-ttu-id="06202-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="06202-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06202-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06202-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06202-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06202-134">CommonParameters</span></span>
<span data-ttu-id="06202-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06202-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06202-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="06202-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06202-137">입력</span><span class="sxs-lookup"><span data-stu-id="06202-137">INPUTS</span></span>

### <span data-ttu-id="06202-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="06202-138">System.String</span></span>

### <span data-ttu-id="06202-139">PSSecurityPartnerProvider에 대 한.</span><span class="sxs-lookup"><span data-stu-id="06202-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="06202-140">출력</span><span class="sxs-lookup"><span data-stu-id="06202-140">OUTPUTS</span></span>

### <span data-ttu-id="06202-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="06202-141">System.Boolean</span></span>

## <span data-ttu-id="06202-142">상속자</span><span class="sxs-lookup"><span data-stu-id="06202-142">NOTES</span></span>

## <span data-ttu-id="06202-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06202-143">RELATED LINKS</span></span>
