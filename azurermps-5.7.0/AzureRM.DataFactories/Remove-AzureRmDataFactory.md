---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
ms.openlocfilehash: 212e0c2ee4863c6d18873a717ff25f6940c34a15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529001"
---
# <span data-ttu-id="35931-101">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="35931-101">Remove-AzureRmDataFactory</span></span>

## <span data-ttu-id="35931-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35931-102">SYNOPSIS</span></span>
<span data-ttu-id="35931-103">Data factory를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="35931-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35931-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35931-104">SYNTAX</span></span>

### <span data-ttu-id="35931-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="35931-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35931-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="35931-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35931-107">설명은</span><span class="sxs-lookup"><span data-stu-id="35931-107">DESCRIPTION</span></span>
<span data-ttu-id="35931-108">**AzureRmDataFactory** cmdlet은 data factory를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="35931-108">The **Remove-AzureRmDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="35931-109">예제의</span><span class="sxs-lookup"><span data-stu-id="35931-109">EXAMPLES</span></span>

### <span data-ttu-id="35931-110">예제 1: data factory 제거</span><span class="sxs-lookup"><span data-stu-id="35931-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzureRmDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="35931-111">이 명령은 ADF 라는 리소스 그룹에서 WikiADF 이라는 data factory를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="35931-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="35931-112">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="35931-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="35931-113">변수</span><span class="sxs-lookup"><span data-stu-id="35931-113">PARAMETERS</span></span>

### <span data-ttu-id="35931-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="35931-114">-DataFactory</span></span>
<span data-ttu-id="35931-115">제거할 **PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35931-115">Specifies the **PSDataFactory** object to remove.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35931-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35931-116">-DefaultProfile</span></span>
<span data-ttu-id="35931-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="35931-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35931-118">-Force</span><span class="sxs-lookup"><span data-stu-id="35931-118">-Force</span></span>
<span data-ttu-id="35931-119">이 cmdlet이 확인을 묻지 않고 데이터 팩토리를 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="35931-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="35931-120">-이름</span><span class="sxs-lookup"><span data-stu-id="35931-120">-Name</span></span>
<span data-ttu-id="35931-121">제거할 데이터 팩터리의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35931-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35931-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35931-122">-ResourceGroupName</span></span>
<span data-ttu-id="35931-123">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35931-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="35931-124">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 데이터 팩터리를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="35931-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35931-125">-확인</span><span class="sxs-lookup"><span data-stu-id="35931-125">-Confirm</span></span>
<span data-ttu-id="35931-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="35931-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35931-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35931-127">-WhatIf</span></span>
<span data-ttu-id="35931-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="35931-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35931-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35931-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35931-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35931-130">CommonParameters</span></span>
<span data-ttu-id="35931-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35931-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35931-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35931-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35931-133">입력</span><span class="sxs-lookup"><span data-stu-id="35931-133">INPUTS</span></span>

### <span data-ttu-id="35931-134">않아야</span><span class="sxs-lookup"><span data-stu-id="35931-134">None</span></span>
<span data-ttu-id="35931-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35931-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="35931-136">출력</span><span class="sxs-lookup"><span data-stu-id="35931-136">OUTPUTS</span></span>

### <span data-ttu-id="35931-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="35931-137">System.Boolean</span></span>

## <span data-ttu-id="35931-138">상속자</span><span class="sxs-lookup"><span data-stu-id="35931-138">NOTES</span></span>
* <span data-ttu-id="35931-139">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="35931-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="35931-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35931-140">RELATED LINKS</span></span>

[<span data-ttu-id="35931-141">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="35931-141">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="35931-142">새로운 AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="35931-142">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)


