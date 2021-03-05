---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: 7dd27544e3304570cf3fbdae861b21eabd300c35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968976"
---
# <span data-ttu-id="113d0-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="113d0-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="113d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="113d0-102">SYNOPSIS</span></span>
<span data-ttu-id="113d0-103">Azure IoT Hub 키를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="113d0-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="113d0-104">구문</span><span class="sxs-lookup"><span data-stu-id="113d0-104">SYNTAX</span></span>

### <span data-ttu-id="113d0-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="113d0-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="113d0-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="113d0-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="113d0-107">설명</span><span class="sxs-lookup"><span data-stu-id="113d0-107">DESCRIPTION</span></span>
<span data-ttu-id="113d0-108">Azure IoT Hub 키를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="113d0-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="113d0-109">예제</span><span class="sxs-lookup"><span data-stu-id="113d0-109">EXAMPLES</span></span>

### <span data-ttu-id="113d0-110">예제 1 주 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="113d0-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="113d0-111">Azure iot Hub의 권한 부여 정책 "testKey"에 대한 기본 키를 다시 생성했습니다.</span><span class="sxs-lookup"><span data-stu-id="113d0-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="113d0-112">예제 2 키 교환</span><span class="sxs-lookup"><span data-stu-id="113d0-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="113d0-113">Azure iot Hub의 권한 부여 정책 "testKey"에 대한 키를 교환합니다.</span><span class="sxs-lookup"><span data-stu-id="113d0-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="113d0-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="113d0-114">PARAMETERS</span></span>

### <span data-ttu-id="113d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="113d0-115">-DefaultProfile</span></span>
<span data-ttu-id="113d0-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="113d0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="113d0-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="113d0-117">-HubId</span></span>
<span data-ttu-id="113d0-118">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="113d0-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="113d0-119">-KeyName</span><span class="sxs-lookup"><span data-stu-id="113d0-119">-KeyName</span></span>
<span data-ttu-id="113d0-120">키의 이름</span><span class="sxs-lookup"><span data-stu-id="113d0-120">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="113d0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="113d0-121">-Name</span></span>
<span data-ttu-id="113d0-122">IotHub의 이름</span><span class="sxs-lookup"><span data-stu-id="113d0-122">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="113d0-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="113d0-123">-RenewKey</span></span>
<span data-ttu-id="113d0-124">키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="113d0-124">Regenerate Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="113d0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="113d0-125">-ResourceGroupName</span></span>
<span data-ttu-id="113d0-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="113d0-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="113d0-127">-확인</span><span class="sxs-lookup"><span data-stu-id="113d0-127">-Confirm</span></span>
<span data-ttu-id="113d0-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="113d0-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="113d0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="113d0-129">-WhatIf</span></span>
<span data-ttu-id="113d0-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="113d0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="113d0-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="113d0-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="113d0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="113d0-132">CommonParameters</span></span>
<span data-ttu-id="113d0-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="113d0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="113d0-134">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="113d0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="113d0-135">입력</span><span class="sxs-lookup"><span data-stu-id="113d0-135">INPUTS</span></span>

### <span data-ttu-id="113d0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="113d0-136">System.String</span></span>

## <span data-ttu-id="113d0-137">출력</span><span class="sxs-lookup"><span data-stu-id="113d0-137">OUTPUTS</span></span>

### <span data-ttu-id="113d0-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="113d0-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="113d0-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="113d0-139">NOTES</span></span>

## <span data-ttu-id="113d0-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="113d0-140">RELATED LINKS</span></span>
