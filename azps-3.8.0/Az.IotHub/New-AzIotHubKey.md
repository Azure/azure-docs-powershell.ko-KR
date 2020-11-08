---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: cc843ca942ae79fe76e1dd50e76c876e4d05b5ac
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043805"
---
# <span data-ttu-id="f615d-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="f615d-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="f615d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f615d-102">SYNOPSIS</span></span>
<span data-ttu-id="f615d-103">Azure IoT Hub 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f615d-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="f615d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f615d-104">SYNTAX</span></span>

### <span data-ttu-id="f615d-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f615d-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f615d-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f615d-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f615d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f615d-107">DESCRIPTION</span></span>
<span data-ttu-id="f615d-108">Azure IoT Hub 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f615d-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="f615d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f615d-109">EXAMPLES</span></span>

### <span data-ttu-id="f615d-110">예제 1 기본 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="f615d-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="f615d-111">Azure iot hub의 권한 부여 정책 "testKey"에 대 한 기본 키를 다시 생성 했습니다.</span><span class="sxs-lookup"><span data-stu-id="f615d-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="f615d-112">예제 2 스와핑 키</span><span class="sxs-lookup"><span data-stu-id="f615d-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="f615d-113">Azure iot hub의 권한 부여 정책 "testKey"에 대 한 키 바꾸기.</span><span class="sxs-lookup"><span data-stu-id="f615d-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="f615d-114">변수</span><span class="sxs-lookup"><span data-stu-id="f615d-114">PARAMETERS</span></span>

### <span data-ttu-id="f615d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f615d-115">-DefaultProfile</span></span>
<span data-ttu-id="f615d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f615d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f615d-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="f615d-117">-HubId</span></span>
<span data-ttu-id="f615d-118">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="f615d-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f615d-119">-KeyName</span><span class="sxs-lookup"><span data-stu-id="f615d-119">-KeyName</span></span>
<span data-ttu-id="f615d-120">키 이름</span><span class="sxs-lookup"><span data-stu-id="f615d-120">Name of the Key</span></span>

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

### <span data-ttu-id="f615d-121">-이름</span><span class="sxs-lookup"><span data-stu-id="f615d-121">-Name</span></span>
<span data-ttu-id="f615d-122">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f615d-122">Name of the IotHub</span></span>

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

### <span data-ttu-id="f615d-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="f615d-123">-RenewKey</span></span>
<span data-ttu-id="f615d-124">키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f615d-124">Regenerate Key.</span></span>

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

### <span data-ttu-id="f615d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f615d-125">-ResourceGroupName</span></span>
<span data-ttu-id="f615d-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f615d-126">Resource Group Name</span></span>

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

### <span data-ttu-id="f615d-127">-확인</span><span class="sxs-lookup"><span data-stu-id="f615d-127">-Confirm</span></span>
<span data-ttu-id="f615d-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f615d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f615d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f615d-129">-WhatIf</span></span>
<span data-ttu-id="f615d-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f615d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f615d-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f615d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f615d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f615d-132">CommonParameters</span></span>
<span data-ttu-id="f615d-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f615d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f615d-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f615d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f615d-135">입력</span><span class="sxs-lookup"><span data-stu-id="f615d-135">INPUTS</span></span>

### <span data-ttu-id="f615d-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f615d-136">System.String</span></span>

## <span data-ttu-id="f615d-137">출력</span><span class="sxs-lookup"><span data-stu-id="f615d-137">OUTPUTS</span></span>

### <span data-ttu-id="f615d-138">IotHub를 호출 합니다. Pssharedaccess서명 Authorizationrule</span><span class="sxs-lookup"><span data-stu-id="f615d-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="f615d-139">상속자</span><span class="sxs-lookup"><span data-stu-id="f615d-139">NOTES</span></span>

## <span data-ttu-id="f615d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f615d-140">RELATED LINKS</span></span>
