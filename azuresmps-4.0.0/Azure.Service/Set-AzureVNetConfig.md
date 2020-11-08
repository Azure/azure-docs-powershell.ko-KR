---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 895F9A5F-D48F-403D-BD8F-72D72D420690
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97bb3e07f5c6df25e7c03c167cc4cb49c25f9414
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045787"
---
# <span data-ttu-id="ee402-101">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="ee402-101">Set-AzureVNetConfig</span></span>

## <span data-ttu-id="ee402-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee402-102">SYNOPSIS</span></span>
<span data-ttu-id="ee402-103">Azure 클라우드 서비스에 대 한 가상 네트워크 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee402-103">Updates the virtual network settings for an Azure cloud service.</span></span>

## <span data-ttu-id="ee402-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ee402-104">SYNTAX</span></span>

```
Set-AzureVNetConfig [-ConfigurationPath] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ee402-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ee402-105">DESCRIPTION</span></span>
<span data-ttu-id="ee402-106">**Set-AzureVNetConfig** cmdlet은 네트워크 구성 파일 (netcfg)에 대 한 경로를 지정 하 여 현재 Azure 구독에 대 한 네트워크 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee402-106">The **Set-AzureVNetConfig** cmdlet updates the network configuration for the current Azure subscription by specifying a path to a network configuration file (.netcfg).</span></span>
<span data-ttu-id="ee402-107">네트워크 구성 파일은 구독 내에서 클라우드 서비스에 대 한 DNS 서버 및 서브넷을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee402-107">The network configuration file defines DNS servers and subnets for cloud services within a subscription.</span></span>

## <span data-ttu-id="ee402-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ee402-108">EXAMPLES</span></span>

### <span data-ttu-id="ee402-109">예제 1: 로컬 파일에 대 한 Azure 구독 네트워크 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="ee402-109">Example 1: Update the network configuration of the Azure subscription to a local file</span></span>
```
PS C:\> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="ee402-110">이 명령은 현재 Microsoft Azure 구독에 대 한 네트워크 구성을 로컬 파일 "c:\temp\MyAzNets.netcfg"에 해당 하는 것으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee402-110">This command updates the network configuration of the current Microsoft Azure subscription to that in the local file "c:\temp\MyAzNets.netcfg".</span></span>

### <span data-ttu-id="ee402-111">예제 2: Azure 구독을 설정한 다음 네트워크 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee402-111">Example 2: Set the Azure subscription and then update the network configuration</span></span>
```
PS C:\> $SubsId = "5bea2bc2-88a5-44b8-abe1-3e76733b6783"
C:\PS> $Cert = Get-Item cert:\LocalMachine\MY\82F105B2DA81149204A6257A9A91EC452B8C52C3
C:\PS> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="ee402-112">이 예제에서는 Microsoft Azure 구독을 설정한 다음 로컬 파일 "c:\temp\MyAzNets.netcfg"에 정의 된 구성을 사용 하 여 해당 구독의 네트워크 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee402-112">This example sets the Microsoft Azure subscription, and then updates the network configuration of that subscription using the configuration defined in the local file "c:\temp\MyAzNets.netcfg".</span></span>

## <span data-ttu-id="ee402-113">변수</span><span class="sxs-lookup"><span data-stu-id="ee402-113">PARAMETERS</span></span>

### <span data-ttu-id="ee402-114">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="ee402-114">-ConfigurationPath</span></span>
<span data-ttu-id="ee402-115">네트워크 구성 파일 (netcfg)의 경로와 파일 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee402-115">Specifies the path and file name of a network configuration file (.netcfg).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee402-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ee402-116">-InformationAction</span></span>
<span data-ttu-id="ee402-117">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee402-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ee402-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ee402-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ee402-119">하기로</span><span class="sxs-lookup"><span data-stu-id="ee402-119">Continue</span></span>
- <span data-ttu-id="ee402-120">숨기기</span><span class="sxs-lookup"><span data-stu-id="ee402-120">Ignore</span></span>
- <span data-ttu-id="ee402-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="ee402-121">Inquire</span></span>
- <span data-ttu-id="ee402-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ee402-122">SilentlyContinue</span></span>
- <span data-ttu-id="ee402-123">중지가</span><span class="sxs-lookup"><span data-stu-id="ee402-123">Stop</span></span>
- <span data-ttu-id="ee402-124">대기</span><span class="sxs-lookup"><span data-stu-id="ee402-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee402-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ee402-125">-InformationVariable</span></span>
<span data-ttu-id="ee402-126">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee402-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee402-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="ee402-127">-Profile</span></span>
<span data-ttu-id="ee402-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee402-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ee402-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ee402-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee402-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee402-130">CommonParameters</span></span>
<span data-ttu-id="ee402-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee402-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee402-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee402-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee402-133">입력</span><span class="sxs-lookup"><span data-stu-id="ee402-133">INPUTS</span></span>

## <span data-ttu-id="ee402-134">출력</span><span class="sxs-lookup"><span data-stu-id="ee402-134">OUTPUTS</span></span>

## <span data-ttu-id="ee402-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ee402-135">NOTES</span></span>

## <span data-ttu-id="ee402-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee402-136">RELATED LINKS</span></span>

[<span data-ttu-id="ee402-137">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="ee402-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="ee402-138">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="ee402-138">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="ee402-139">-AzureVNetConfig 제거</span><span class="sxs-lookup"><span data-stu-id="ee402-139">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)


