---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: f05d4142efab5a95cfef43fbc44cf57d0e1e2cf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532242"
---
# <span data-ttu-id="c512a-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="c512a-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="c512a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c512a-102">SYNOPSIS</span></span>
<span data-ttu-id="c512a-103">웹 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c512a-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c512a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c512a-104">SYNTAX</span></span>

### <span data-ttu-id="c512a-105">Azure ML 웹 서비스 리소스를 이름 및 리소스 그룹으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c512a-105">Remove an Azure ML web service resouce by name and resource group.</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c512a-106">개체로 지정 된 Azure ML 웹 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c512a-106">Remove an Azure ML web service specified as an object.</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c512a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c512a-107">DESCRIPTION</span></span>
<span data-ttu-id="c512a-108">리소스 그룹 및 이름에서 참조 하는 Azure 기계 학습 웹 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c512a-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="c512a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c512a-109">EXAMPLES</span></span>

### <span data-ttu-id="c512a-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c512a-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="c512a-111">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="c512a-111">@{paragraph=PS C:\\\>}</span></span>





```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="c512a-112">변수</span><span class="sxs-lookup"><span data-stu-id="c512a-112">PARAMETERS</span></span>

### <span data-ttu-id="c512a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c512a-113">-Force</span></span>
<span data-ttu-id="c512a-114">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c512a-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c512a-115">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="c512a-115">-MlWebService</span></span>
<span data-ttu-id="c512a-116">제거할 웹 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="c512a-116">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Remove an Azure ML web service specified as an object.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c512a-117">-이름</span><span class="sxs-lookup"><span data-stu-id="c512a-117">-Name</span></span>
<span data-ttu-id="c512a-118">제거할 웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c512a-118">The name of the web service to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c512a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c512a-119">-ResourceGroupName</span></span>
<span data-ttu-id="c512a-120">웹 서비스의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="c512a-120">The resource group of the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c512a-121">-확인</span><span class="sxs-lookup"><span data-stu-id="c512a-121">-Confirm</span></span>
<span data-ttu-id="c512a-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c512a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c512a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c512a-123">-WhatIf</span></span>
<span data-ttu-id="c512a-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c512a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c512a-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c512a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c512a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c512a-126">-DefaultProfile</span></span>
<span data-ttu-id="c512a-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c512a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c512a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c512a-128">CommonParameters</span></span>
<span data-ttu-id="c512a-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c512a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c512a-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c512a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c512a-131">입력</span><span class="sxs-lookup"><span data-stu-id="c512a-131">INPUTS</span></span>

### <span data-ttu-id="c512a-132">용</span><span class="sxs-lookup"><span data-stu-id="c512a-132">WebService</span></span>
<span data-ttu-id="c512a-133">' MlWebService ' 매개 변수는 파이프라인에서 ' WebService ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c512a-133">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="c512a-134">출력</span><span class="sxs-lookup"><span data-stu-id="c512a-134">OUTPUTS</span></span>

### <span data-ttu-id="c512a-135">않아야</span><span class="sxs-lookup"><span data-stu-id="c512a-135">None</span></span>

## <span data-ttu-id="c512a-136">상속자</span><span class="sxs-lookup"><span data-stu-id="c512a-136">NOTES</span></span>
<span data-ttu-id="c512a-137">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="c512a-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="c512a-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c512a-138">RELATED LINKS</span></span>

