---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 5a9dc29d9cb078473a777279c5bdb648a1b9388e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213566"
---
# <span data-ttu-id="ea352-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="ea352-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="ea352-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea352-102">SYNOPSIS</span></span>
<span data-ttu-id="ea352-103">IoT 중앙 응용 프로그램을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea352-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="ea352-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea352-104">SYNTAX</span></span>

### <span data-ttu-id="ea352-105">ResourceIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ea352-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea352-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea352-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea352-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea352-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea352-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ea352-108">DESCRIPTION</span></span>
<span data-ttu-id="ea352-109">기존 IoT 중앙 응용 프로그램을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea352-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="ea352-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ea352-110">EXAMPLES</span></span>

### <span data-ttu-id="ea352-111">예제 1 삭제 및 IoT 중앙 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="ea352-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="ea352-112">제공 된 IoT 중앙 응용 프로그램을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea352-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="ea352-113">변수</span><span class="sxs-lookup"><span data-stu-id="ea352-113">PARAMETERS</span></span>

### <span data-ttu-id="ea352-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea352-114">-AsJob</span></span>
<span data-ttu-id="ea352-115">백그라운드에서 cmdlet을 작업으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea352-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="ea352-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea352-116">-DefaultProfile</span></span>
<span data-ttu-id="ea352-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea352-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea352-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea352-118">-InputObject</span></span>
<span data-ttu-id="ea352-119">Iot 중앙 응용 프로그램 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ea352-119">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea352-120">-이름</span><span class="sxs-lookup"><span data-stu-id="ea352-120">-Name</span></span>
<span data-ttu-id="ea352-121">Iot 중앙 응용 프로그램 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea352-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea352-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea352-122">-PassThru</span></span>
<span data-ttu-id="ea352-123">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="ea352-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ea352-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea352-124">-ResourceGroupName</span></span>
<span data-ttu-id="ea352-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea352-125">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea352-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea352-126">-ResourceId</span></span>
<span data-ttu-id="ea352-127">Iot 중앙 응용 프로그램 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="ea352-127">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea352-128">-확인</span><span class="sxs-lookup"><span data-stu-id="ea352-128">-Confirm</span></span>
<span data-ttu-id="ea352-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea352-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea352-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea352-130">-WhatIf</span></span>
<span data-ttu-id="ea352-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ea352-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea352-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea352-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea352-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea352-133">CommonParameters</span></span>
<span data-ttu-id="ea352-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea352-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea352-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea352-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea352-136">입력</span><span class="sxs-lookup"><span data-stu-id="ea352-136">INPUTS</span></span>

### <span data-ttu-id="ea352-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ea352-137">System.String</span></span>

### <span data-ttu-id="ea352-138">PSIotCentralApp를 통해 서 .exe.</span><span class="sxs-lookup"><span data-stu-id="ea352-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="ea352-139">출력</span><span class="sxs-lookup"><span data-stu-id="ea352-139">OUTPUTS</span></span>

### <span data-ttu-id="ea352-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ea352-140">System.Boolean</span></span>

## <span data-ttu-id="ea352-141">상속자</span><span class="sxs-lookup"><span data-stu-id="ea352-141">NOTES</span></span>

## <span data-ttu-id="ea352-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea352-142">RELATED LINKS</span></span>
