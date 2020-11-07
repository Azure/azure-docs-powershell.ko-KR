---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/set-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
ms.openlocfilehash: a9b7dbc962809288979f5293c14fd875081f48bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711672"
---
# <span data-ttu-id="aea22-101">Set-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="aea22-101">Set-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="aea22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aea22-102">SYNOPSIS</span></span>
<span data-ttu-id="aea22-103">IoT 중앙 응용 프로그램에 대 한 메타 데이터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="aea22-103">Updates the metadata for an IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aea22-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aea22-104">SYNTAX</span></span>

### <span data-ttu-id="aea22-105">ResourceIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="aea22-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aea22-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aea22-106">InputObjectParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aea22-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="aea22-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aea22-108">설명은</span><span class="sxs-lookup"><span data-stu-id="aea22-108">DESCRIPTION</span></span>
<span data-ttu-id="aea22-109">IoT 중앙 응용 프로그램에 대 한 메타 데이터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="aea22-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="aea22-110">예제의</span><span class="sxs-lookup"><span data-stu-id="aea22-110">EXAMPLES</span></span>

### <span data-ttu-id="aea22-111">예제 1 업데이트 표시 이름</span><span class="sxs-lookup"><span data-stu-id="aea22-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="aea22-112">기존 IoT 중앙 응용 프로그램에서 표시 이름을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="aea22-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="aea22-113">출력 예:</span><span class="sxs-lookup"><span data-stu-id="aea22-113">Example Output:</span></span>

<span data-ttu-id="aea22-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/Iotcentral/MyAppResourceName Name: MyAppResourceName 유형: Microsoft. IoTCentral/Iotcentral 위치: westus Tag: Sku: Microsoft Azure. p r o: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My를 통해 새 사용자 지정 표시 이름 하위 도메인: MyAppSubdomain 서식 파일: iotc-default@1.0.0 SubscriptionId: Xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aea22-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="aea22-115">변수</span><span class="sxs-lookup"><span data-stu-id="aea22-115">PARAMETERS</span></span>

### <span data-ttu-id="aea22-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aea22-116">-AsJob</span></span>
<span data-ttu-id="aea22-117">백그라운드에서 cmdlet을 작업으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="aea22-117">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="aea22-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea22-118">-DefaultProfile</span></span>
<span data-ttu-id="aea22-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aea22-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aea22-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="aea22-120">-DisplayName</span></span>
<span data-ttu-id="aea22-121">Iot 중앙 응용 프로그램의 사용자 지정 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aea22-121">Custom Display Name of the Iot Central Application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea22-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aea22-122">-InputObject</span></span>
<span data-ttu-id="aea22-123">Iot 중앙 응용 프로그램 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="aea22-123">Iot Central Application Input Object.</span></span>

```yaml
Type: PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aea22-124">-이름</span><span class="sxs-lookup"><span data-stu-id="aea22-124">-Name</span></span>
<span data-ttu-id="aea22-125">Iot 중앙 응용 프로그램 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aea22-125">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea22-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aea22-126">-ResourceGroupName</span></span>
<span data-ttu-id="aea22-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aea22-127">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea22-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aea22-128">-ResourceId</span></span>
<span data-ttu-id="aea22-129">Iot 중앙 응용 프로그램 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="aea22-129">Iot Central Application Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aea22-130">태그</span><span class="sxs-lookup"><span data-stu-id="aea22-130">-Tag</span></span>
<span data-ttu-id="aea22-131">Iot 중앙 응용 프로그램 리소스 태그</span><span class="sxs-lookup"><span data-stu-id="aea22-131">Iot Central Application Resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea22-132">-확인</span><span class="sxs-lookup"><span data-stu-id="aea22-132">-Confirm</span></span>
<span data-ttu-id="aea22-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aea22-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aea22-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aea22-134">-WhatIf</span></span>
<span data-ttu-id="aea22-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aea22-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aea22-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aea22-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aea22-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea22-137">CommonParameters</span></span>
<span data-ttu-id="aea22-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aea22-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea22-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea22-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea22-140">입력</span><span class="sxs-lookup"><span data-stu-id="aea22-140">INPUTS</span></span>

### <span data-ttu-id="aea22-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aea22-141">System.String</span></span>
### <span data-ttu-id="aea22-142">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="aea22-142">System.Collections.Hashtable</span></span>
### <span data-ttu-id="aea22-143">PSIotCentralApp를 통해 서 .exe.</span><span class="sxs-lookup"><span data-stu-id="aea22-143">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="aea22-144">출력</span><span class="sxs-lookup"><span data-stu-id="aea22-144">OUTPUTS</span></span>

### <span data-ttu-id="aea22-145">PSIotCentralApp를 통해 서 .exe.</span><span class="sxs-lookup"><span data-stu-id="aea22-145">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="aea22-146">상속자</span><span class="sxs-lookup"><span data-stu-id="aea22-146">NOTES</span></span>

## <span data-ttu-id="aea22-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aea22-147">RELATED LINKS</span></span>
