---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 30926eaad6447f109b1755d419be0b3931a76054
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94227002"
---
# <span data-ttu-id="fc681-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="fc681-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="fc681-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc681-102">SYNOPSIS</span></span>
<span data-ttu-id="fc681-103">Iot Hub에서 대상 IoT 장치 모듈의 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc681-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="fc681-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc681-104">SYNTAX</span></span>

### <span data-ttu-id="fc681-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fc681-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc681-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fc681-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc681-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fc681-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc681-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fc681-108">DESCRIPTION</span></span>
<span data-ttu-id="fc681-109">Azure IoT Hub 내에 포함 된 대상 IoT 디바이스의 지정 된 모듈 또는 모든 모듈의 연결 문자열을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc681-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="fc681-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fc681-110">EXAMPLES</span></span>

### <span data-ttu-id="fc681-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fc681-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="fc681-112">Iot Hub의 대상 IoT 장치에 대 한 모든 모듈 연결 문자열을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc681-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="fc681-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="fc681-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="fc681-114">Iot Hub의 대상 IoT 장치에 대 한 보조 모듈 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc681-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="fc681-115">변수</span><span class="sxs-lookup"><span data-stu-id="fc681-115">PARAMETERS</span></span>

### <span data-ttu-id="fc681-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc681-116">-DefaultProfile</span></span>
<span data-ttu-id="fc681-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc681-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc681-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="fc681-118">-DeviceId</span></span>
<span data-ttu-id="fc681-119">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="fc681-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc681-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc681-120">-InputObject</span></span>
<span data-ttu-id="fc681-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="fc681-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc681-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fc681-122">-IotHubName</span></span>
<span data-ttu-id="fc681-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="fc681-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc681-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="fc681-124">-KeyType</span></span>
<span data-ttu-id="fc681-125">Auth에 대 한 공유 액세스 정책 키 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="fc681-125">Shared access policy key type for auth.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc681-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="fc681-126">-ModuleId</span></span>
<span data-ttu-id="fc681-127">대상 모듈 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="fc681-127">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc681-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc681-128">-ResourceGroupName</span></span>
<span data-ttu-id="fc681-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc681-129">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc681-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc681-130">-ResourceId</span></span>
<span data-ttu-id="fc681-131">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="fc681-131">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc681-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc681-132">CommonParameters</span></span>
<span data-ttu-id="fc681-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc681-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc681-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc681-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc681-135">입력</span><span class="sxs-lookup"><span data-stu-id="fc681-135">INPUTS</span></span>

### <span data-ttu-id="fc681-136">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="fc681-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fc681-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fc681-137">System.String</span></span>

## <span data-ttu-id="fc681-138">출력</span><span class="sxs-lookup"><span data-stu-id="fc681-138">OUTPUTS</span></span>

### <span data-ttu-id="fc681-139">IotHub. PSModuleConnectionString/. \*</span><span class="sxs-lookup"><span data-stu-id="fc681-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="fc681-140">상속자</span><span class="sxs-lookup"><span data-stu-id="fc681-140">NOTES</span></span>

## <span data-ttu-id="fc681-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc681-141">RELATED LINKS</span></span>
